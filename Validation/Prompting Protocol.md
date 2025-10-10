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
