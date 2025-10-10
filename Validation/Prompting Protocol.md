# Prompting Protocol: Mock Interview Validation Study

## 1. Objective
This document outlines the protocol used to systematically test the capabilities of existing general-purpose AI language and conversational models for the task of conducting mock technical interviews. The primary goal is to identify specific gaps in functionality, realism, and feedback quality, thereby validating the need for a specialized tool like MockSy.

## 2. Tools Under Evaluation
A diverse set of commercially available AI tools were selected to cover different model families and interaction modalities:
*   **ChatGPT (GPT-4o):** A leading large language model known for its strong conversational and reasoning abilities.
*   **Meta AI (Llama 3):** A powerful open-weights model integrated into social platforms, tested for its conversational flow.
*   **Google AI (Gemini Family):** A multimodal model from Google, tested for its directness and feedback capabilities.
*   **Grok AI (Grok-1):** A conversational AI with a distinct personality, tested for its ability to handle technical nuance.

## 3. Scenarios and Prompts

Our testing was structured around three distinct cases designed to probe the limits of these generalist AIs.

### **Case 1: The Typical Case (Baseline Performance)**
*   **Objective:** To establish a baseline by evaluating the AI's ability to handle a standard, well-defined mock interview request.
*   **Scenario:** A junior data engineer candidate preparing for a role at a top tech company.
*   **Core Prompt:**
    ```
    "I want you to act as an expert interviewer for an engineering role at Netflix. I am a candidate for a junior data engineer position. I want you to conduct a mock interview with me. Ask me three technical questions and two behavioral questions. Ask the questions one by one and wait for my response."
    ```
*   **Tested On:** ChatGPT, Google AI.

### **Case 2: The Edge Case (Handling Inaccurate & Vague Information)**
*   **Objective:** To assess the AI's domain expertise and its ability to correct misinformation or probe for more detail when given intentionally weak, inaccurate, or vague answers.
*   **Scenario:** A candidate provides technically flawed or superficial answers to complex questions.
*   **Example Interaction:** Providing an inaccurate definition of Spark (Meta AI) or a generic definition of a real-time dashboard without implementation details (Grok AI).
*   **Tested On:** Meta AI, Grok AI.

### **Case 3: The Failure Case (Conversational Robustness & Feedback Quality)**
*   **Objective:** To intentionally try to break the conversational flow and test the quality and integrity of the AI's feedback mechanism when faced with irrelevant input or direct challenges.
*   **Scenario 1 (Irrelevant Input):** The candidate responds to a technical debugging question with nonsensical, off-topic quotes.
*   **Scenario 2 (Feedback Refusal):** The candidate directly presses the AI for a quantitative score and a hiring decision, testing its ability to provide actionable, evaluative feedback.
*   **Tested On:** ChatGPT (Misleading), Google AI.

The table below summarizes our key findings from these conversations.

| AI Tool Tested 🤖 | Scenario & Goal 🎯                                           | Key Finding 🤔                                                                                             | Implication for MockSy 💡                                                                                     |
| :--------------- | :----------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------- |
| **ChatGPT (GPT-4o)** | ✅ **Baseline Test:** Can it handle a standard interview?        | ⚠️ Gave a wildly inflated score **(85-90/100)** for mediocre answers. It acts more like a people-pleaser than an objective coach. | MockSy **must** provide calibrated, realistic, and honest feedback, not just positive reinforcement.              |
| **Google AI (Gemini)** | 🔎 **Feedback Integrity Test:** Will it provide a real score?  | 🛑 **Flatly refused** to provide a quantitative score or a hiring decision, stating it was unable to. This is a dead end for users tracking progress. | MockSy's core value is providing the **measurable metrics** that general tools actively avoid.                      |
| **Meta AI (Llama 3)** | 🧠 **Technical Accuracy Test:** How does it handle incorrect info? | 📖 Corrected a technically inaccurate answer but failed to **probe deeper** into the candidate's flawed reasoning. The feedback was superficial. | MockSy needs a deeper, **role-specific context** to truly assess a candidate's thought process.                 |
| **Grok AI (Grok-1)** | 🧭 **Guidance Test:** Can it guide a struggling candidate?      | 🎁 When the candidate was vague, it **gave away the ideal answer** instead of guiding them. This turns a test into a lecture. | MockSy must be engineered to **prompt and guide**, not simply provide solutions, to foster real learning.         |
| **ChatGPT (GPT-4o)** | 🌪️ **Robustness Stress Test:** What happens with nonsensical input? | 😵 **Completely derailed** by irrelevant answers, becoming confused and eventually hallucinating that a valid response was given. | MockSy must use a **state-managed, controlled interview flow** to prevent derailment and maintain a realistic session. |

### The Takeaway

The conclusion is clear: while general AIs are incredible tools, they are **not effective interview coaches.** They lack the ability to provide honest feedback, maintain a controlled session, and assess deep expertise. This evidence forms the foundation of MockSy's mission to build a tool that truly prepares candidates for success.

---
