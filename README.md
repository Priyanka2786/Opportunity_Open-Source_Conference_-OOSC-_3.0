# Opportunity_Open-Source_Conference_-OOSC-_3.0
Opportunity Open-Source Conference (OOSC) 3.0 is a premier event dedicated to fostering innovation, collaboration, and learning in the open-source community.

 # Conversational Agent Onboarding - Prototype

This project is a **FastAPI-based prototype backend** for a conversational agent that streamlines **customer onboarding**.  
It supports configurable questions, session management, document upload with OCR (mocked), photo capture with liveliness detection (mocked), OTP verification, and final application submission.  

---

## 🚀 Features
- Human-like conversational onboarding flow  
- Config-driven question framework  
- Multi-step session handling  
- Document upload + OCR (mock)  
- Photo capture + liveliness detection (mock)  
- OTP send & verify (mock: always `1234`)  
- Unified application submission payload  
- MongoDB (via `motor`) or in-memory fallback  

---

## 📦 Setup

### 1. Clone the repository
```bash
git clone https://github.com/your-repo/conversational-agent.git
cd conversational-agent

