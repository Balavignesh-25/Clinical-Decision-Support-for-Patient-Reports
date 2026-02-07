# Secure Medical Report Analysis 

This project implements a **secure, end-to-end medical document analysis pipeline** using **Groq’s LLaMA 3.1** model in **Google Colab**, following **industry best practices for PHI handling and API security**.

It processes patient PDF reports, extracts clinical information using OCR and LLMs, anonymizes sensitive data, and generates structured medical insights for clinical decision support.

---

## 🚀 Key Features

- 📄 PDF medical report ingestion
- 🔍 OCR-based text extraction (Tesseract + Poppler)
- 🔐 PHI anonymization with reversible token mapping
- 🧠 Structured clinical event extraction using LLaMA 3.1
- 📊 Chronological medical history synthesis
- 🚨 Abnormality detection with severity assessment
- 🔄 Optional PHI re-identification (controlled)
- 🔑 Secure API key handling (no hardcoding)
- ☁️ Google Colab & GitHub safe

---

## 🏗️ System Architecture (High Level)
```
PDF Reports
↓
OCR (Tesseract)
↓
PHI Anonymization
↓
LLaMA 3.1 (Groq API)
↓
Structured JSON Outputs
↓
Clinical Summary & Analysis
```

## 🔐 API Key & Security (IMPORTANT)

### Why this matters
Medical data + API keys = **high-risk**  
This project is designed to be **safe for GitHub** and compliant with secure development practices.

### ✅ Google Colab (Recommended)

1. Open the notebook in **Google Colab**
2. Click **🔑 Secrets** (left sidebar)
3. Add a new secret:
   - **Name**: `GROQ_API_KEY`
   - **Value**: your Groq API key
4. Enable **Notebook access**
5. Restart the runtime
6. Run all cells

> ⚠️ The API key is **never stored in code or notebooks** and is **not committed to GitHub**.

---

## 🖥️ Local Development (Optional)

If you want to run locally:

### Set environment variable

**Linux / macOS**
```bash
export GROQ_API_KEY=your_api_key_here
```
Windows (PowerShell)
```
setx GROQ_API_KEY "your_api_key_here"
```

---

## 🧪 What the Pipeline Extracts

### From historical reports

- Past diseases
- Previous medications
- Prior consultations

### From the latest report

- Abnormal lab values
- Severity classification (mild / moderate / severe)
- General (non-prescriptive) recommendations
- Doctor consultation urgency

---

## 🔒 PHI Handling Strategy

- Sensitive fields (names, phone numbers, emails) are tokenized
- Tokens are passed to the LLM instead of raw PHI
- Optional controlled re-identification is supported
- Designed with healthcare privacy principles in mind

##⚠️ Disclaimer

- This project is intended for educational and research purposes only.
- It is not a medical diagnosis system
- It does not replace licensed medical professionals
- Any recommendations generated are informational only

---

## 🧠 Engineering Highlights

- Deterministic LLM outputs (temperature=0)
- Safe JSON parsing to prevent hallucinated responses
- Modular, testable functions
- Environment-aware secret management
- GitHub & recruiter friendly

---

## 🚀 Future Enhancements

- RAG with clinical guidelines (WHO / NICE / CDC)
- FastAPI backend for hospital systems
- Streamlit dashboard for doctors
- Confidence scoring for extracted insights
- Audit logs for compliance

---

## ⭐ Final Note

This repository demonstrates real-world ML engineering practices:
- Security-first mindset
- Healthcare-aware design
- Production-oriented code structure

---
