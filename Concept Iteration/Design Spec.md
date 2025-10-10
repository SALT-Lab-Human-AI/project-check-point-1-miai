## 1. Project Overview

**Project Name:** *MockSy*

**Goal:**  
To help job seekers practice and improve interview performance through simulated, interactive interview sessions.  
The tool aims to reduce anxiety, encourage reflection, and build confidence through realistic, personalized practice.

---

### Technology Direction (Preliminary)

| Area | Current Consideration | Purpose |
| :--- | :--- | :--- |
| **Frontend** | A modern web framework (e.g., Next.js or React) | Enables fast, interactive UI for interviews and dashboards. |
| **Styling / UI** | Tailwind CSS or equivalent component library | Ensures responsive and accessible design. |
| **Voice Interaction** | Prototype voice agent (to be finalized) | Simulates interviewer conversations and captures responses. |
| **Backend / Data** | Lightweight cloud database (e.g., Firebase / Supabase) | Stores user data, interviews, and feedback. |
| **AI Generation** | Large Language Model API (Gemini / GPT-based) | Generates interview questions and structured feedback. |
| **Utilities** | TypeScript, Schema Validation Library | Provides type safety and consistent data flow. |

*(Exact stack will be finalized during implementation.)*

---

## 2. Core Features (Concept Stage)

1. **Authentication** — Basic login/signup to personalize sessions and track progress.  
2. **Interview Generation** — AI generates questions tailored to role, level, and tech stack.  
3. **Interview Session** — Simulated conversation with an AI interviewer (voice).  
4. **Data Storage** — Session data and feedback stored securely for later review.  
5. **Dashboard** — Displays previous attempts and performance summaries.  
6. **Feedback & Scoring** — Post-interview feedback with metrics such as confidence, communication, and technical clarity.

*(Each feature will be validated through user testing and prototyped incrementally.)*

---

## 3. User Journeys

### A. New User — Onboarding & Interview Setup
1. User visits the platform and signs up.  
2. After authentication, lands on a personal dashboard.  
3. Clicks **“Start a New Interview”** to begin setup.  
4. Selects interview parameters (role, type, level, stack, number of questions).  
5. The system generates a set of customized questions using an AI model.  
6. The user begins a practice session — a voice-based configuration.  
7. On completion, a summary card appears on the dashboard showing interview metadata.

### B. Returning User — Review & Feedback
1. User opens dashboard to view past sessions.  
2. Selects a completed interview to read feedback.  
3. System displays overall score and per-category breakdown.  
4. User reviews strengths and weaknesses.  
5. Optionally retakes the interview or starts a new one with modified parameters.

---

## 4. Task Flows & Key Screens (Prototype Level)

### 4.1 Authentication
**Screens:** Sign Up · Sign In  
- Collects name, email, and password.  
- Validates inputs; shows inline error messages.  
- Successful sign-up redirects to the dashboard.  
- Placeholder authentication in early prototype (no full OAuth yet).

---

### 4.2 Dashboard
**Purpose:** Central hub showing ongoing and completed interviews.  

| Element | Function |
| :--- | :--- |
| **Navigation Bar** | Logo + account controls. |
| **Call to Action (CTA)** | “Start Interview” button linking to setup page. |
| **Interview Cards** | List previous interviews with role, date, and score (if available). |
| **Quick Stats** | Optional: show average score or streak summary. |

---

### 4.3 Interview Setup & Session
**Core Interaction Screen:**  
- Collects interview preferences (role, level, stack, etc.).  
- Displays loading state while AI prepares questions.  
- Once ready, initiates the simulated interview:  
  - Voice or chat interface engages the user.  
  - Transcript or chat history shown live on screen.  
  - Option to pause or end the interview anytime.  
- After session ends, transitions to a feedback summary screen.

*(The voice agent prototype currently uses a placeholder conversational interface. A dedicated API will be chosen once validation confirms feasibility.)*

---

### 4.4 Feedback Screen
**Purpose:** Provide immediate, structured feedback after each session.  

| Section | Description |
| :--- | :--- |
| **Overall Score** | Summarizes user performance (0–100). |
| **Category Breakdown** | Scores for Communication, Technical Depth, Problem Solving, and Confidence. |
| **Strengths** | Short list of what went well. |
| **Areas to Improve** | Actionable suggestions for next attempt. |
| **Navigation Buttons** | “Retake Interview” and “Back to Dashboard.” |

---

## 5. Accessibility & UX Guidelines
- Minimalistic layout that works well on both laptop and mobile.  
- Consistent button placement and intuitive progress indicators.  
- Visual feedback for microphone and connection states.  
- Clear typography with adequate contrast (dark theme).  

---

## 6. Privacy & Safety Considerations
- User data stored securely; no sharing of personal information.  
- Voice and transcript data anonymized before analysis.  
- Clear disclosures about AI usage and data retention.  
- Early prototypes will use mock data until full privacy review.  

---

## 7. Future Directions
- **Enhanced Feedback Loop:** Graphical performance tracking over time.  
- **Company-Specific Modes:** e.g., “Amazon Behavioral Round” or “FAANG System Design.”  
- **Multi-Modal Interface:** Combine voice and code editor for technical interviews.  
- **Peer Practice Mode:** Connect two users for live practice with AI moderation.  

---

*This document reflects the concept-validation stage (Checkpoint 2).  
It focuses on user experience, feasibility exploration, and early feedback incorporation — final stack and integrations will be locked after CP3 implementation testing.*
