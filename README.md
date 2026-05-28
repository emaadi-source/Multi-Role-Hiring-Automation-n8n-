# 🤖 AI Hiring Automation System

**Screen SWE & BDM candidates automatically. Save 20 hours/week.**

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
