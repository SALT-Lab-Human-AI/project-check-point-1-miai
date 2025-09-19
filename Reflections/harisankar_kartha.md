# AI Mock Interview Research Summaries (Extended)

This repository contains structured notes and insights from additional research papers closely aligned to our project: an AI Voice Agent Enabled Mock Interview Platform using Gemini for question generation and feedback.

---

## 📄 Paper 1: *MACH: My Automated Conversation coacH*  
**Citation:** Hoque, M. E., Courgeon, M., Martin, J.-C., Mutlu, B., & Picard, R. W. (2013). *MACH: My Automated Conversation coacH.* Proceedings of UbiComp ’13. https://doi.org/10.1145/2493432.2493502  

### Summary (4–6 sentences)  
MACH is a virtual agent that delivers mock job interviews while analyzing facial expressions, speech, and prosody. After each session, it provides structured post-interview feedback (e.g., speaking rate, filler words, smiling). In a study with 90 students, MACH users improved interview performance compared to peers who practiced alone or watched videos. Participants valued the agent’s credibility and specific behavioral cues. This shows how automated systems can reduce anxiety and improve practice outcomes.  

### 3 Insights I Learned  
1. Post-interview feedback is more effective than interrupting users mid-session.  
2. Simple cues like speaking pace and filler words provide actionable improvement signals.  
3. Natural back-channeling (nodding, small responses) increases agent believability.  

### 2 Limitations/Risks  
1. Focused mainly on nonverbal behavior, not on answer content.  
2. Results were limited to a single student population.  

### 1 Concrete Idea for Our Project  
Keep feedback **structured but simple**, focusing on a few clear delivery/content metrics after each session to avoid overwhelming users.  

---

## 📄 Paper 2: *Automatic Skill-Oriented Question Generation and Interview Question Recommendation*  
**Citation:** Qin, C., Zhu, H., Shen, D., Sun, Y., Yao, K., Wang, P., & Xiong, H. (2024). *Automatic Skill-Oriented Question Generation and Interview Question Recommendation.* ACM Transactions on Information Systems, 42(1). https://doi.org/10.1145/3604552  

### Summary (4–6 sentences)  
This paper introduces DuerQues, a system that mines skill entities from large datasets, generates interview questions with neural models, and recommends them using graph-based methods. It leverages external sources like community Q&A and click logs to ensure relevance. Experiments showed strong results in creating targeted, skill-specific interview questions at scale. This demonstrates how AI can generate both breadth and depth of content for interviews.  

### 3 Insights I Learned  
1. Skill-specific question generation makes practice far more relevant than generic sets.  
2. Mining job-related skills from external text keeps questions updated.  
3. Recommendations can ensure appropriate difficulty and focus per user.  

### 2 Limitations/Risks  
1. Relies on large proprietary datasets, which may not be available in small projects.  
2. Automatically generated questions can still contain bias or irrelevant phrasing.  

### 1 Concrete Idea for Our Project  
Use **Gemini prompts** to generate questions directly from user inputs (role, stack, level) and apply lightweight filters to ensure technical relevance.  

---

## 📄 Paper 3: *Voice AI in Firms: A Natural Field Experiment on Automated Job Interviews*  
**Citation:** Jabarian, B., & Henkel, L. (2025). *Voice AI in Firms: A Natural Field Experiment on Automated Job Interviews.* SSRN Working Paper, 89 pp. https://doi.org/10.2139/ssrn.5395709  

### Summary (4–6 sentences)  
This large field experiment (≈70,000 applicants) tested replacing human-led interviews with AI voice agents. Applicants were randomly assigned to human, AI, or choice-based interviews, while recruiters still made final decisions. Results showed AI-led interviews improved hiring outcomes (offers, starts, retention) and 78% of applicants preferred the AI option. Candidate satisfaction was comparable across groups. The study demonstrates that AI interviews can be credible, accepted, and effective in practice.  

### 3 Insights I Learned  
1. Applicants are open to AI-led interviews, reducing adoption concerns.  
2. AI interviews often elicit more job-relevant responses than human ones.  
3. Candidate satisfaction and perceived fairness remain high with AI agents.  

### 2 Limitations/Risks  
1. Technical glitches occurred in some sessions, showing reliability is key.  
2. Findings come from one firm and may not generalize to all roles or industries.  

### 1 Concrete Idea for Our Project  
Focus on making our **voice agent feel natural and professional**, since this strongly affects candidate comfort and engagement.  

---

## 📄 Paper 4: *ROC Speak: Semi-Automated Personalized Feedback on Nonverbal Behavior*  
**Citation:** Fung, M., Jin, Y., Zhao, R., & Hoque, M. E. (2015). *ROC Speak: Semi-Automated Personalized Feedback on Nonverbal Behavior from Recorded Videos.* Proceedings of UbiComp ’15. https://doi.org/10.1145/2750858.2804265  

### Summary (4–6 sentences)  
ROC Speak helps users practice interviews or presentations by recording themselves and receiving a mix of automated and short crowd-sourced feedback. It analyzed facial expressions, prosody, and voice modulation. In a 10-day study with 56 participants, users who got ROC Speak feedback showed measurable improvements in communication and confidence. The system demonstrated the effectiveness of combining AI cues with human-like evaluations for skill-building.  

### 3 Insights I Learned  
1. Even basic delivery metrics (pace, filler count) provide helpful improvement signals.  
2. Tracking progress across sessions motivates continued practice.  
3. Semi-automated feedback can build user trust.  

### 2 Limitations/Risks  
1. Required human reviewers, limiting scalability.  
2. Focused mainly on delivery, not technical accuracy.  

### 1 Concrete Idea for Our Project  
Add **simple delivery insights** (e.g., filler count, speech speed) to Gemini’s transcript-based content feedback.  

---

## 📄 Paper 5: *An RCT of Virtual Reality Job Interview Training for Individuals with Serious Mental Illness*  
**Citation:** Smith, M. J., et al. (2022). *An RCT of Virtual Reality Job Interview Training for Individuals with Serious Mental Illness in IPS Supported Employment.* Psychiatric Services, 73(9), 1027–1038. https://doi.org/10.1176/appi.ps.202100516  

### Summary (4–6 sentences)  
This randomized controlled trial evaluated a VR-based interview training tool for 90 individuals with serious mental illness. Participants practiced interviews with a virtual interviewer and received structured feedback. Compared to controls, VR-JIT participants significantly improved interview performance and had higher employment rates after six months. The findings show the long-term value of simulated practice for real-world outcomes.  

### 3 Insights I Learned  
1. Repeated practice in safe environments builds confidence and skill.  
2. Even anxious or vulnerable users accept and benefit from virtual interview systems.  
3. Improvements in practice can translate into real job outcomes.  

### 2 Limitations/Risks  
1. VR hardware requirements limit accessibility.  
2. Findings may not generalize to broader job-seeker populations.  

### 1 Concrete Idea for Our Project  
Highlight the ability to **retake interviews endlessly** in PrepWise, since repetition is proven to build both confidence and real-world readiness.  

---
