🧪 **AI Lab Report Analyzer — Vision-OCR + Urdu Voice Summary**

> **Production AI system** that photographs any lab test report and 
> instantly generates a complete patient-friendly analysis with 
> plain language explanations, normal/abnormal flagging, and 
> Urdu voice summary — deployed at Pakistan's largest digital 
> health platform.

![GPT-4o](https://img.shields.io/badge/GPT--4o_Vision-412991?style=flat-square&logo=openai&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-000000?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![ElevenLabs](https://img.shields.io/badge/ElevenLabs_TTS-000000?style=flat-square&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazon-aws&logoColor=white)

---

## 📊 Production Impact

| Metric | Value |
|--------|-------|
| Patient support queries reduced | 35% |
| Languages supported | English + Urdu Voice |
| Report types handled | Blood tests, urine, thyroid, liver, kidney + more |
| Input method | Photo of printed lab report |
| Deployment | AWS · Docker · Production |

---

## 🏗️ LangGraph Pipeline Architecture

![System Architecture](architecture/system-architecture.png)

> **Smart conditional routing** — if the uploaded image cannot be 
> processed (poor quality or invalid document), the pipeline 
> gracefully rejects. On success: vision extraction → PDF 
> generation → Urdu voice → final summary.

---

## ⚡ Key Features

- **GPT-4o Vision extraction** — processes real-world lab report 
  photos handling lighting variation, angles, and print quality
- **Per-test analysis** — each individual test result analyzed 
  separately with plain language explanation
- **Normal/Abnormal flagging** — automatic detection with clear 
  health implication for the patient
- **Urdu voice summary** — ElevenLabs TTS generates audio 
  explanation in Urdu for low-literacy patients
- **End-to-end pipeline** — raw photo → structured analysis → 
  audio output in a single flow
- **No doctor appointment needed** — patients understand their 
  own results instantly

---

## 🔄 How It Works

```mermaid
sequenceDiagram
    participant P as 👤 Patient
    participant API as FastAPI
    participant V as GPT-4o Vision
    participant A as Analyzer Agent
    participant T as ElevenLabs TTS

    P->>API: Upload photo of lab report
    API->>V: Send image for extraction
    V-->>A: Extracted test values + reference ranges
    A->>A: Analyze each test — normal/abnormal check
    A-->>API: Structured analysis ready
    API->>T: Send analysis text in Urdu
    T-->>API: Urdu audio file generated
    API-->>P: ✅ Patient-friendly report + Urdu voice summary
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Vision & Extraction | GPT-4o Vision |
| Agent Orchestration | LangChain |
| Voice Generation | ElevenLabs TTS |
| Backend | FastAPI, Python |
| PDF Processing | pdfplumber |
| Deployment | Docker, AWS |

---

## 📸 Live Demo

> Screenshots and demo coming soon

---

## 🎥 Demo Video

> Demo video coming soon

---

> ⚠️ **Note:** This repository showcases the architecture and design 
> of a production system built at Oladoc. Source code is proprietary.

---

## 📫 Contact

**Adnan Abdullah** — Agentic AI Engineer & AI Team Lead

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/adnan-abdullah-700899b)
[![Email](https://img.shields.io/badge/Gmail-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:muhammad.adnannust@gmail.com)

---

*Built with GPT-4o Vision + ElevenLabs · Deployed at Pakistan's 
largest digital health platform · 35% reduction in patient 
support queries*
