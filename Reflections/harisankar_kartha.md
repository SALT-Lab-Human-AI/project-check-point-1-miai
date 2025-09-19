# AI Mock Interview Research Summaries (Extended)

This repository contains structured notes and insights from additional research papers closely aligned to our project: an AI Voice Agent Enabled Mock Interview Platform using Gemini for question generation and feedback.

# 📚 Literature Reflections

## Paper 1: *Will You Trust Me More Than ChatGPT? Evaluating LLM-Generated Code Feedback for Mock Technical Interviews* (2025)

**Citation + Link**  
Vaishampayan, S., & Brown, C. (2025). *Will You Trust Me More Than ChatGPT? Evaluating LLM-Generated Code Feedback for Mock Technical Interviews.* IEEE/ACM 18th International Conference on Cooperative and Human Aspects of Software Engineering (CHASE). https://doi.org/10.1109/CHASE66643.2025.00018  


### 📑 Summary (4–6 sentences)  
This study investigates the usefulness and trustworthiness of LLM-generated feedback on code in mock technical interview settings. The authors built a platform powered by ChatGPT where candidates solved algorithmic problems, and feedback was delivered in two modes: human-administered (Wizard-of-Oz style) and automated. Across 46 participants, feedback was mostly accurate (~83%) and highly useful (~91%), but trust significantly dropped when users knew feedback came directly from ChatGPT. The findings highlight a paradox: while AI feedback is effective for learning, candidates still prefer a human “face” to mediate it.  

### 💡 3 Insights I Learned  
1. Accuracy ≠ trust: Even when AI feedback was correct, candidates trusted it less if it was clearly automated.  
2. Human-AI collaboration boosts acceptance — adding light human mediation improved perceived reliability.  
3. Feedback on time/space complexity and optimization was especially valued, showing where LLMs add unique value over peers.  

### ⚠️ 2 Limitations/Risks  
1. Small, single-site sample (students only) limits generalization to industry professionals.  
2. AI hallucinations and overly generalized suggestions reduced credibility, even if rare.  

### 🎯 1 Concrete Idea for MockSy  
Include a **“feedback framing layer”** — e.g., present AI feedback in structured, human-like report templates rather than raw text. This could increase trust without major infrastructure changes.  

---

## Paper 2: *AI-Driven Real-Time Interview Simulation App with Voice Recognition and Facial Analysis* (2025)

**Citation + Link**  
Jagtap, S. R., Kulkarni, V., Pachorkar, Y., Taur, O., Gupta, S., & Pujeri, U. (2025). *AI-Driven Real-Time Interview Simulation App with Voice Recognition and Facial Analysis.* *Indian Journal of Science and Technology, 18*(25), 2058–2066. https://doi.org/10.17485/IJST/v18i25.760  


### 📑 Summary (4–6 sentences)  
This paper introduces an Android application that combines real-time **facial expression tracking, voice analysis, and ChatGPT-driven question generation** to simulate realistic interviews. The app leverages Google ML Kit for facial analysis, Google Teachable Machine for custom voice models, and ChatGPT API for dynamic dialogue. Testing showed ~70% of users reported improved confidence, eye contact, and communication after repeated sessions. Compared to earlier tools, this platform uniquely integrates multimodal feedback (verbal + nonverbal), making simulations more immersive and holistic.  

### 💡 3 Insights I Learned  
1. Multimodal feedback (voice + face) enhances realism and captures non-verbal skills often missed in AI prep tools.  
2. Mobile-first design improves accessibility, letting candidates practice anywhere.  
3. Real-time adaptive feedback (based on past performance) is a differentiator from static Q&A apps.  

### ⚠️ 2 Limitations/Risks  
1. Current version lacks multilingual support and cultural adaptation, limiting broader usability.  
2. No VR/AR integration, which could further boost immersion.  

### 🎯 1 Concrete Idea for MockSy  
While MockSy focuses on **voice + LLM feedback**, a **future extension** could include lightweight non-verbal tracking (e.g., speech pacing or pause detection) to approximate behavioral feedback without requiring full facial analysis.  

---
## Paper: *AI-Enhanced HR Interview Simulation for Realistic Candidate Assessment* (2025)

**Citation + Link**  
Sarumathi, S., Gowthaman, R. L., Sultana, A., & Sabareesh, M. B. (2025). *AI-Enhanced HR Interview Simulation for Realistic Candidate Assessment.* Proceedings of the 3rd International Conference on Intelligent Data Communication Technologies and Internet of Things (IDCIoT-2025). IEEE. https://doi.org/10.1109/IDCIOt64235.2025.10915193  


### 📑 Summary (4–6 sentences)  
This paper proposes an AI-driven HR interview simulation system that generates **personalized questions from a candidate’s resume and job description**, simulating realistic recruiter-style interviews. It integrates **Gemini-based LLMs** for adaptive questioning, facial expression analysis via CNNs, and **voice sentiment analysis** via RNNs to evaluate both cognitive and emotional performance. Reinforcement learning dynamically adjusts difficulty, digging deeper into strengths or weaknesses. The system also evaluates **ATS compliance** in resumes, provides real-time feedback, and outputs structured interview reports. Reported benefits include scalability (handling many candidates simultaneously), fairness through reduced bias, and holistic assessment combining both technical and affective traits.  


### 💡 3 Insights I Learned  
1. Resume + job description parsing enables highly personalized, context-specific interview questions.  
2. Emotion and behavior tracking (facial + vocal cues) add depth to assessment beyond technical correctness.  
3. Scalability is a major advantage — the system can screen large candidate pools consistently without fatigue or bias.  


### ⚠️ 2 Limitations/Risks  
1. Heavy reliance on facial and vocal analysis could introduce cultural bias or misinterpretation of behaviors.  
2. Complexity and cost of multimodal AI systems may hinder adoption for smaller organizations.  


### 🎯 1 Concrete Idea for MockSy  
Instead of full facial analysis, **lightweight ATS-style resume parsing** could be integrated into MockSy to **generate more tailored questions** from user-uploaded resumes. This keeps scope manageable while adding personalization, directly inspired by this paper’s resume-driven approach.  

---

## Paper: *Talent Tracer – AI Driven Interview Preparation Engine for Job Seekers using LLMs* (2025)

**Citation + Link**  
Akshaya, V., Vejaysundaram, R., & Santhosh, H. (2025). *Talent Tracer – AI Driven Interview Preparation Engine for Job Seekers using LLMs.* Proceedings of the 11th International Conference on Communication and Signal Processing (ICCSP 2025). IEEE. https://doi.org/10.1109/ICCSP64183.2025.11088608  


### 📑 Summary (4–6 sentences)  
This paper presents *Talent Tracer*, an AI-based interview preparation platform designed to improve candidates’ **technical, behavioral, and soft skills**. The system parses resumes and job descriptions to identify skills and gaps, then generates customized interview questions using transformer-based models (GPT, T5, BART). Candidates can respond in **text, audio, or video**, with each input type analyzed by specialized AI models: DeepSeek NLP for text, Whisper ASR for speech, and CNN classifiers for real-time video evaluation (facial expressions, posture, gestures). Feedback is compiled into a comprehensive report with strengths, weaknesses, and targeted recommendations. Compared to existing systems, Talent Tracer offers **multimodal evaluation and explainable AI**, producing up to 15% performance improvement in accuracy, precision, and recall.  


### 💡 3 Insights I Learned  
1. Multimodal input (text, audio, video) provides richer feedback than single-mode systems.  
2. Resume + job description parsing ensures **questions are tailored** to candidate background and role requirements.  
3. Real-time video evaluation (body language, gestures, posture) gives deeper insights into confidence and professionalism.  


### ⚠️ 2 Limitations/Risks  
1. Heavy reliance on CNN models for body language risks bias (e.g., cultural variations in gestures or posture).  
2. System complexity may hinder adoption outside large institutions with sufficient compute resources.  


### 🎯 1 Concrete Idea for MockSy  
MockSy could adopt **resume + JD parsing** to personalize question sets while staying lightweight. Instead of full video analysis, it could integrate simpler add-ons like **speech pacing or filler-word detection** to approximate behavioral feedback without the heavy compute load of CNN models.  

