# 📄 Resume Intelligence AI

A modern, serverless Resume Analyzer that evaluates resumes against job descriptions using NLP-based similarity scoring, skill extraction, and ATS optimization logic.

Built with AWS Lambda, API Gateway, and DynamoDB, featuring a sleek glassmorphism UI with real-time analysis and popup-based results.


## 🚀 Features

- 📄 Upload PDF resume or paste text  
- 🎯 Match resume with job description  
- 📊 ATS score calculation  
- 🧠 Skill extraction & gap detection  
- 💡 Smart suggestions for improvement  
- ⚡ Real-time analysis via API  
- ☁️ Fully serverless backend (AWS)  
- 🪟 Interactive popup result UI  


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

## 🏗️ Live Architecture Flow

```mermaid
graph TD
    %% Define Styles
    classDef user fill:#ffffff,stroke:#333,stroke-width:2px,color:#333;
    classDef frontend fill:#e1f5fe,stroke:#01579b,stroke-width:2px,color:#01579b;
    classDef aws_api fill:#fff3e0,stroke:#e65100,stroke-width:2px,color:#e65100;
    classDef aws_lambda fill:#f3e5f5,stroke:#4a148c,stroke-width:2px,color:#4a148c;
    classDef aws_db fill:#e8f5e9,stroke:#1b5e20,stroke-width:2px,color:#1b5e20;
    classDef results fill:#fff9c4,stroke:#fbc02d,stroke-width:2px,color:#000;

    %% Workflow Nodes
    User((👤 User Browser)) 
    
    subgraph Client_Side [Frontend Environment]
        UI[🎨 UI: Glass & Neon Design]
        PDF[📄 PDF.js Parsing]
        Fetch[📡 Fetch API Call]
    end

    subgraph Gateway_Layer [Traffic Control]
        AGW[🛰️ API Gateway: REST + CORS]
    end

    subgraph Logic_Core [Intelligence Engine: AWS Lambda]
        Clean[🧹 Text Cleaning & Stopwords]
        Token[🔡 Tokenization]
        Sim[📐 Cosine Similarity Logic]
        Skills[🔍 Regex Skill Extraction]
        ATS[📊 ATS & Suggestion Engine]
    end

    subgraph Storage_Layer [Data Persistence]
        DB[(📦 DynamoDB: Analysis Results)]
    end

    subgraph Final_View [Feedback Loop]
        Popup[✨ Frontend Popup UI]
        Score[✅ Final Metrics: ATS / Match / Gaps]
    end

    %% Connection Logic
    User -->|Upload / Input| UI
    UI --> PDF
    PDF --> Fetch
    Fetch --> AGW
    AGW --> Clean
    Clean --> Token
    Token --> Sim
    Sim --> Skills
    Skills --> ATS
    ATS -->|PutItem| DB
    ATS -->|JSON Response| Fetch
    Fetch --> Popup
    Popup --> Score
    Score -->|Visual Feedback| User

    %% Apply Styles
    class User user;
    class UI,PDF,Fetch frontend;
    class AGW aws_api;
    class Clean,Token,Sim,Skills,ATS aws_lambda;
    class DB aws_db;
    class Popup,Score results;
