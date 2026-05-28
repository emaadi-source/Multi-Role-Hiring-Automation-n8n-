# 🤖 AI Hiring Automation System

**Screen SWE & BDM candidates automatically. Save 20 hours/week.**

---

<img width="1232" height="566" alt="95b6493e-31c7-4b96-b40a-27ec490bd89c" src="https://github.com/user-attachments/assets/ac0f4e41-bb5c-43b9-9528-6043b1ec30ad" />


---

## The Problem

Hiring teams spend 15-20 minutes manually reviewing each application. Decisions are inconsistent. Candidates wait days for responses.

## The Solution

An n8n workflow that evaluates every candidate using AI and sends instant personalized emails based on their score.

---

## How It Works

**Every 30 minutes:**
- Pulls new applications from SWE and BDM Google Forms
- Downloads resumes from Google Drive
- Sends candidate data to Groq AI (Llama 3.3 70B)
- Stores score, classification, and analysis in a master sheet

**Every hour:**
- Strong candidates (score 70+) → Interview email + Calendar invite
- Average candidates (score 40-69) → Hiring manager notification
- Weak candidates (score below 40) → Professional rejection email

---

## AI Evaluation

The AI returns a structured JSON for every candidate:

```json
{
  "score": 85,
  "classification": "strong",
  "summary": "Strong React experience, 5 years at FAANG",
  "strengths": ["Python", "System design", "Leadership"],
  "concerns": ["Limited cloud experience"]
}

### Tech Stack
| Tool | Purpose |
| --- | --- |
| n8n | Workflow automation |
| Google Forms | Application intake |
| Google Sheets | Data storage |
| Groq API | AI evaluation - free tier |
| Gmail + Calendar | Communication |

### What's Included
| File | Description |
| --- | --- |
| HiringAutomation.json | Complete n8n workflow - 29 nodes |
| Walkthrough_Report.pdf | Technical documentation |
| README.md | This file |

### Quick Setup
- Create SWE and BDM Google Forms linked to sheets
- Create a master sheet with required columns
- Get free API keys: Groq + Google OAuth2
- Import JSON into n8n
- Replace placeholder IDs and API keys
- Activate workflow

### Impact
| Metric | Before | After |
| --- | --- | --- |
| Time per app | 15-20 min | 30 sec |
| Response time | 3-5 days | < 1 hour |
| Manager workload | 100% apps | Only average |
