<!-- Logo -->
<p align="center">
  <img src="Mocksy Logo.png" alt="Mocksy Logo" width="200"/>
</p>

<!-- Project Title -->
<h1 align="center">🚀 MockSy</h1>

<!-- Tagline -->
<p align="center"><i>Your personal AI-powered mock interview companion</i></p>


<!-- Badges -->
<p align="center">
  <a href="https://opensource.org/licenses/Apache-2.0">
    <img src="https://img.shields.io/badge/License-Apache_2.0-blue.svg" alt="License"/>
  </a>
  <img src="https://img.shields.io/badge/For-Students-pink.svg" alt="For Students"/>
  <img src="https://img.shields.io/badge/Tech-Next.js-black.svg" alt="Next.js"/>
  <img src="https://img.shields.io/badge/Backend-Firebase-yellow.svg" alt="Firebase"/>
  <img src="https://img.shields.io/badge/AI-Gemini-brightgreen.svg" alt="Gemini AI"/>
</p>

---

## 📌 Problem Statement and Why It Matters  

The core challenge this project tackles is a familiar one: going blank during a coding interview on a question you knew the answer to, only to think afterward, *“I should have said this instead.”*  

This moment of regret is common across all career stages and often stems from inadequate preparation. Without realistic practice, even capable candidates can struggle to showcase their skills effectively, leaving them anxious and underconfident.  

This problem matters because **interview performance is a decisive factor in career growth**. A strong interview can open doors to dream jobs and competitive opportunities, while a weak one can shut them. Employers aren’t just assessing technical knowledge—they’re also evaluating:  

- Clarity of thought  
- Problem-solving under pressure  
- Communication skills  

Candidates who lack structured, practical preparation risk underselling themselves and missing out on pivotal career moves.  

This project aims to change that. By providing a platform for realistic, targeted interview practice, it helps candidates:  

- Refine their responses  
- Boost confidence  
- Consistently present their best selves  

Ultimately, the system makes candidates **better at interviews**.  

## 🌱 Initial Concept & Value Proposition

MockSy is an AI-powered voice agent mock interview platform where users generate custom interview sessions (role, experience level, tech stack, number of questions) then practice via real-time voice interaction 🎤. After each session, MockSy delivers structured feedback—including scores for communication, technical depth, problem solving, and confidence—so users can understand their weaknesses and improve over time. Using Gemini for question generation and Vapi for voice interaction, MockSy aims to deliver realistic, scalable practice without the need for scheduling human interviewers.

MockSy’s value lies in two main strengths. First, it gives users unlimited, personalized practice tuned to their goals—reducing anxiety and helping them perform their best 💪. Second, it provides actionable, objective feedback rather than generic encouragement, enabling targeted improvements. By combining role-specific customization, voice realism, and detailed feedback, MockSy bridges the gap between static prep tools and expensive coaching—making high-quality interview practice accessible to all.

## 🎯 Target Users  

The **AI Mock Interview System** is designed for anyone preparing for job interviews, including:  

- **Students** seeking their first professional role  
- **Experienced professionals** aiming to upskill or transition into new opportunities  

Its flexibility ensures it supports candidates *“no matter where you are in your career.”*  

## 🛠️ Proposed Core User Tasks

- **🔐 Secure Authentication**  
  Users can create an account and log in securely, protecting access and user data.

- **🎨 Personalized Interview Creation**  
  Through a conversational setup, users can tailor interviews by:  
  &nbsp;&nbsp;&nbsp;&nbsp;• Role (Full Stack, Frontend, Backend)  
  &nbsp;&nbsp;&nbsp;&nbsp;• Type (Behavioral, Technical, Mixed)  
  &nbsp;&nbsp;&nbsp;&nbsp;• Experience level (Junior, Senior)  
  &nbsp;&nbsp;&nbsp;&nbsp;• Number of questions  
  &nbsp;&nbsp;&nbsp;&nbsp;• Tech stack (e.g. JS, React, Next.js)

- **🎤 Real-Time Mock Interview Sessions**  
  Users engage with an AI voice agent that uses back-channeling (e.g. “mhm”) and emotional modulation to simulate realistic interviews.

- **📊 Detailed Performance Feedback**  
  After each session, users see:  
  &nbsp;&nbsp;&nbsp;&nbsp;• Overall score  
  &nbsp;&nbsp;&nbsp;&nbsp;• Breakdowns (communication, technical depth, problem-solving, confidence)  
  &nbsp;&nbsp;&nbsp;&nbsp;• Strengths & areas to improve

- **🔄 Practice & Iteration**  
  Users can retake interviews freely to adjust parameters and try new challenges.

- **📂 Review Interview Metadata & History**  
  All previous interviews are saved with metadata (role, tech stack, type, date) so users can revisit setups and track their growth.

---
## ⚙️ Proposed Tech Stack

- **Frontend & Core Framework**
  - Next.js (App Router, TurboPack) for full-stack web app
  - TypeScript for type-safe maintainable code
  - ESLint + Zod + React Hook Form for clean forms & validation

- **UI & Design**
  - Tailwind CSS (dark theme, v4) for responsive styling
  - shadcn/ui for accessible pre-built components
  - Sonner for toasts & alerts
  - Day.js for date formatting

- **Backend & Auth**
  - Firebase Authentication (email/password, secure session cookies)
  - Firestore for user + interview data
  - Firebase Admin SDK & Client SDK for secure server + client ops
  - Next.js Server Actions for safe DB interactions

- **AI & Voice Components**
  - **Vapi** for real-time voice agent (sub-500ms latency, back-channeling, emotion)
  - **Gemini AI** for generating interview questions & structured feedback
  - Vercel AI SDK for integrating Gemini into workflows

- **Deployment**
  - Vercel for fast, reliable deployment

---

## Competitive Landscape: Existing Tools & Their Shortcomings

| Tool / Platform           | What They Do Well                                                                          | What They Miss Compared to  MockSy                                  |
|---------------------------|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| **Pramp / Exponent Practice** | Peer-to-peer live mock interviews, both technical & behavioral practice. | Feedback quality depends heavily on peer; no voice-agent realism; no automated question generation tailored by role/tech stack. |
| **Interviewing.io**         | Expert human interviewers; detailed, actionable feedback; many technical problem types. | High cost; limited availability of sessions; less flexibility for beginners; no fully automated voice agent delivering mock interviews. |
| **HireVue**                 | AI assessments, video interviewing, skills validation in hiring workflows.        | More focused on hiring / assessment than deliberate practice; feedback often not transparent; less customizable for individual practice parameters. |
---

## 🚀 Project Milestones ( Proposed )

### 1️⃣ Foundational Setup & UI/UX (Weeks 2–3)  
**Tasks:** Initialize project with Next.js + TypeScript, set up Tailwind CSS + Shadcn UI, organize file structure, apply global styles, ensure responsive design. Build sign-in/sign-up forms with validation, navigation, and Figma-based UI.  
**Deliverables:** Responsive app layout with authentication pages and primary navigation.  


### 2️⃣ Backend & Authentication (Weeks 4–5)  
**Tasks:** Configure Firebase (Auth + Firestore) for secure authentication and data storage. Implement server actions for sign-up, sign-in, session handling, and persistence.  
**Deliverables:** User accounts stored in Firestore, protected routes, and secure authentication flow.  



### 3️⃣ Homepage & Interview Display (Weeks 6–7)  
**Tasks:** Develop homepage with **“Your Interviews”** and **“Take an Interview”** sections. Create reusable `InterviewCard` component. Implement Firestore data fetching with parallel requests.  
**Deliverables:** Dynamic homepage showing personalized and general interview cards.  



### 4️⃣ AI Interview Generation (Weeks 8–9)  
**Tasks:** Integrate **Vapi** for AI voice and **Gemini AI** for question generation. Build conversational workflows to capture interview parameters (role, type, level, stack, # of questions). Create API endpoint to store generated questions in Firestore.  
**Deliverables:** Functional **Interview Generation** page with AI-assisted customization and stored interviews.  



### 5️⃣ Mock Interview Session (Weeks 9–10)  
**Tasks:** Implement `Agent` component for live sessions. Configure Vapi to use stored questions, manage call states, and handle real-time transcription.  
**Deliverables:** Interactive voice-based mock interviews with live transcript. 🎤  



### 6️⃣ Feedback Generation & Display (Weeks 10–11)  
**Tasks:** Use **Gemini AI** to analyze transcripts and generate structured feedback (scores, strengths, areas for improvement). Store results in Firestore. Build a **Feedback Page** for results display.  
**Deliverables:** Comprehensive feedback view with scores, category breakdowns, and actionable insights. 📊  



### 7️⃣ Deployment & Refinement (Week 12)  
**Tasks:** Deploy on **Vercel**, configure production environment variables, run final testing, and fix bugs.  
**Deliverables:** Fully deployed, production-ready **AI Mock Interview System** accessible online. 🌐  


---

## 👥 Roles & Responsibilities  

- **Aditya** will focus on **frontend development, authentication, and AI integration** (Next.js UI, Firebase Auth, Vapi + Gemini workflows).  
- **Hari** will handle **Firestore integration, backend logic, deployment, and documentation** (data storage/retrieval, server actions, Vercel setup, doc reviews).  
