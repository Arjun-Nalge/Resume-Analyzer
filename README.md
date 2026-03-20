# 📄 Resume Intelligence AI

A modern, serverless Resume Analyzer that evaluates resumes against job descriptions using NLP-based similarity scoring, skill extraction, and ATS optimization logic.

Built with AWS Lambda, API Gateway, and DynamoDB, featuring a sleek glassmorphism UI with real-time analysis and popup-based results.

---

## 🚀 Features

- 📄 Upload PDF resume or paste text  
- 🎯 Match resume with job description  
- 📊 ATS score calculation  
- 🧠 Skill extraction & gap detection  
- 💡 Smart suggestions for improvement  
- ⚡ Real-time analysis via API  
- ☁️ Fully serverless backend (AWS)  
- 🪟 Interactive popup result UI  

---

## 🏗️ Live Architecture Flow
# 📄 Resume Intelligence AI

A modern, serverless Resume Analyzer that evaluates resumes against job descriptions using NLP-based similarity scoring, skill extraction, and ATS optimization logic.

Built with AWS Lambda, API Gateway, and DynamoDB, featuring a sleek glassmorphism UI with real-time analysis and popup-based results.

---

## 🚀 Features

- 📄 Upload PDF resume or paste text  
- 🎯 Match resume with job description  
- 📊 ATS score calculation  
- 🧠 Skill extraction & gap detection  
- 💡 Smart suggestions for improvement  
- ⚡ Real-time analysis via API  
- ☁️ Fully serverless backend (AWS)  
- 🪟 Interactive popup result UI  

---

## 🏗️ Live Architecture Flow
User (Browser)
│
│ Upload Resume / Enter Job Description
▼
Frontend (HTML + CSS + JavaScript)
│
│ ├─ PDF Parsing (PDF.js)
│ ├─ UI Rendering (Glass + Neon Design)
│ └─ API Call (Fetch)
▼
API Gateway (REST API)
│
│ Handles Routing + CORS
▼
AWS Lambda (Python Backend)
│
│ ├─ Text Cleaning (Stopword Removal)
│ ├─ Tokenization
│ ├─ Cosine Similarity (JD Match)
│ ├─ Skill Extraction (Regex)
│ ├─ ATS Score Calculation
│ └─ Suggestion Engine
▼
Amazon DynamoDB
│
│ Stores Analysis Results
▼
Lambda Response (JSON)
│
▼
Frontend Popup UI
│
▼
User Sees:

ATS Score
Match Percentage
Skill Gaps
Suggestions


---

## 🧱 Tech Stack

### Frontend
- HTML5  
- CSS3 (Glassmorphism + Neon UI)  
- JavaScript (Vanilla)  
- PDF.js  

### Backend
- Python (AWS Lambda)  
- REST API (API Gateway)  

### Cloud & Storage
- AWS Lambda  
- Amazon API Gateway  
- Amazon DynamoDB  

---

## ⚙️ How It Works

1. User uploads resume or pastes text  
2. PDF is parsed using PDF.js (if uploaded)  
3. Resume and job description sent to backend via API  
4. Backend:
   - Cleans and tokenizes text  
   - Computes cosine similarity  
   - Extracts skills from both inputs  
   - Calculates ATS score based on skill match  
5. Results stored in DynamoDB  
6. Response returned and displayed in popup UI  

---

## 📊 Scoring Logic

- **ATS Score**  
  Based on percentage of required skills matched  

- **JD Match Score**  
  Cosine similarity between resume and job description  

- **Profile Score**  
  Average of ATS Score and JD Match Score  

## 🧠 What This Project Demonstrates

- Serverless architecture design
- API integration and CORS handling
- NLP fundamentals (tokenization + similarity)
- Frontend + backend integration
- Real-world AWS deployment

## Author
Arjun Nalge - DevOps Engineer

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/arjun-nalge-313642398)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?logo=github)](https://github.com/Arjun-Nalge/Arjun-Nalge.git)
