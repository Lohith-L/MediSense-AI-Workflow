# 🏥 MediSense AI Workflow

An agentic healthcare workflow built on **Supervity Auto** to transform complex medical reports into simple, actionable health guidance for Indian patients.

## 🔗 Live Workflow
[Open the Supervity workflow](https://auto.supervity.ai/u/alpha/agent/workflow/019d261c-b5fe-7000-ae3d-46f40ea16e7f?tab=Workflow)

---

## 🚨 Problem

Many people cannot understand terms like **HbA1c**, **eGFR**, or other medical values on their lab reports.

Health literacy gaps delay treatment and increase preventable risk. MediSense AI is designed to bridge that gap by turning medical report data into clear, practical guidance.

---

## 💡 Solution

MediSense AI transforms:

**Medical Report PDF → Structured Analysis → Research-backed Recommendations → Patient-friendly PDF → Email Delivery**

It helps patients receive:
- simple health summaries
- abnormal value explanations
- Indian diet and lifestyle recommendations
- doctor visit guidance
- retest schedules
- a final report directly in email

---

## ⚙️ Architecture

### Multi-agent workflow
1. Medical Data Extraction
2. Lab Results Analyzer
3. Research Agent
4. Recommendation Agent
5. Report Generator
6. Email Delivery Agent
7. Master Orchestrator
8. Google Sheets Logging

---

## 🤖 Agent Breakdown

### Agent 1 — Medical Data Extraction
Extracts structured data from uploaded medical report PDFs.

### Agent 2 — Medical Lab Results Analyzer
Analyzes extracted values, detects abnormalities, and produces a health score.

### Agent 3 — Research Agent
Researches flagged conditions with:
- plain-language explanation
- common causes
- Indian foods to eat
- foods to avoid
- lifestyle changes
- warning symptoms
- specialist recommendations
- government scheme awareness

### Agent 4 — Recommendation Agent
Generates:
- 7-day Indian diet plan
- exercise plan
- next-step checklist
- doctor questions
- retest schedule

### Agent 5 — Report Generator
Builds a patient-friendly full health report and converts it into PDF.

### Agent 6 — Email Delivery Agent
Sends the personalized report via Outlook.

### Master Orchestrator
Coordinates the entire flow from upload to delivery and logs execution to Google Sheets.

---

## 🌍 Key Features

- 10 Indian language support
- patient-friendly summaries
- health score generation
- Indian diet recommendations
- doctor guidance
- PDF report generation
- Outlook delivery
- OneDrive report storage
- Google Sheets reporting log

---

## 🛠 Tech Stack

- **Platform:** Supervity Auto
- **Storage:** OneDrive
- **Email:** Microsoft Outlook
- **Logging:** Google Sheets
- **Workflow Style:** Multi-agent orchestration

---

## 📁 Repository Structure

```text
MediSense-AI-Workflow/
│
├── README.md
├── agents/
│   ├── agent-3-research.md
│   ├── agent-4-recommendation.md
│   ├── agent-5-report-generator.md
│   ├── agent-6-email-delivery.md
│   └── master-orchestrator.md
│
├── prompts/
│   └── full-prompts.md
│
├── demo/
│   └── linkedin-post.md
│
└── outputs/
    └── sample-output-note.md
```

---

## 🎥 Demo Positioning

This project was built as a real-world healthcare accessibility workflow for **CodeQuest 2026 Round 2**, focused on solving medical report literacy in India.

---

## 🚀 Why This Matters

This is not just automation.

This is **AI for Bharat** — designed around:
- low health literacy
- regional language accessibility
- affordability
- simple, practical healthcare guidance

---

## 👨‍💻 Author

**Lohith L**

---

## 📣 LinkedIn Post

The supporting LinkedIn post for this build is included in `demo/linkedin-post.md`.

---

## ⚠️ Disclaimer

MediSense AI is built for health awareness and assistance. It is **not a substitute for professional medical advice, diagnosis, or treatment**.
