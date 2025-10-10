# How MockSy Will Try to Address Key Gaps

The Validation study revealed that general-purpose AI models are fundamentally ill-suited for the specialized task of mock interviewing. This document outlines the specific technical architecture and strategies MockSy employs to solve the critical gaps we identified, ensuring a reliable, effective, and specialized training experience.

---

## 1. Addressing the Feedback Gap: From People-Pleaser to Objective Evaluator

**The Problem:** General LLMs are optimized for agreeable conversation, not for critical evaluation. This results in overly positive and unhelpful feedback.

**Our Solution:** We are engineering a dedicated **Feedback Generation Engine** that constrains the AI to act as a neutral, data-driven evaluator.

### Technical Steps:

1.  **Strictly-Typed, Structured Output:** Do not request a simple text response. Instead, our backend makes a dedicated API call to Gemini with a system prompt that commands it to return a JSON object adhering to a predefined schema. We will use a library like **Zod** to validate this output, guaranteeing that we always receive consistent, structured data.

    *A sample of the expected JSON output:*
    ```json
    {
      "overallScore": 82,
      "categories": {
        "technicalDepth": { "score": 7, "feedback": "Your pipeline design was solid but lacked detail on fault tolerance." },
        "communication": { "score": 9, "feedback": "You articulated your thoughts clearly and concisely." },
        "problemSolving": { "score": 8, "feedback": "Good use of standard tools, but consider mentioning trade-offs more." }
      },
      "strengths": ["Clear explanation of Kafka's role.", "Good choice of storage tiers."],
      "areasForImprovement": ["Provide more specific data cleaning techniques beyond dropping rows.", "Elaborate on SQL query optimization using execution plans."]
    }
    ```

2.  **Engineered Evaluator Persona & Rubric:** The system prompt for our feedback endpoint is meticulously engineered. It instructs the AI to adopt the persona of a **"Strict but Fair Hiring Manager"** and evaluate the transcript against a clear, embedded rubric. This removes ambiguity and prevents the AI from defaulting to its native agreeable nature.

---

## 2. Addressing the Controlled Session Gap

**The Problem:** A general chatbot has no concept of an "interview flow" and can be easily derailed by unexpected user input.

**Our Solution:** We are implementing a finite state machine (FSM) to manage the interview's progression and are using a purpose-built voice agent platform (such as Vapi) designed for goal-oriented conversation.

### Technical Steps:

*   **State-Managed Interview Flow:** Our system is not a single, open-ended conversation. We manage the interview's progression through a defined state machine: `[Greeting] -> [Asking_Technical_Q1] -> [Listening_For_Answer_1] -> [Transitioning] -> [Closing]`. This ensures the conversation stays on track. If a user provides an irrelevant answer, the system, while in the `Listening_For_Answer` state, is programmed to recognize the non-sequitur and re-prompt gracefully (e.g., *"I'm sorry, I don't think I followed that. Could you please elaborate on your technical process?"*).

*   **Preventing the AI from "Giving Away the Answer":** Our state management strictly controls the AI's behavior. When the agent is in a listening state, its instructions are to probe and ask clarifying questions, not to provide the solution. While it can be programmed to offer a small hint if a candidate is stuck, it is explicitly forbidden from giving the answer away—a common failure mode we observed in our testing.

---

## 3. Addressing the Domain Expertise Gap: From Generalist to Specialist

**The Problem:** A general LLM's knowledge is a mile wide and an inch deep, making it ineffective for interviewing in niche or senior roles.

**Our Solution:** We address this through a combination of dynamic prompt augmentation and curated content, ensuring a high degree of technical relevance.

### Technical Steps:

1.  **Dynamic, Role-Specific System Prompts:** When a user creates an interview for a "Senior Backend Engineer (Elixir)," the system prompt sent to Gemini is dynamically constructed. It includes this specific context and instructs the model to generate questions focused on relevant, advanced concepts for that role (e.g., BEAM VM, OTP, GenServers).

2.  **Curated Question Banks in Firestore:** Instead of relying solely on the LLM to generate questions from scratch, we will maintain a vetted question bank within our Firestore database. Each question will be tagged by role, technology, and difficulty. The system can then be configured to pull a mix of these pre-vetted questions and fresh LLM-generated questions, ensuring a baseline of quality and relevance that a general model alone cannot guarantee.
