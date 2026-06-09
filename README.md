# n8n-missed-lead-recovery

# Missed Lead Recovery System

An AI-powered n8n workflow that detects unresponded leads and automatically
sends personalised follow-up emails — reducing revenue lost to slow response times.

---

## The Problem

Most small businesses lose leads not because of bad products or pricing, but
because nobody followed up in time. A lead fills in a form, gets no response
within a few hours, and moves on to a competitor.

Manual follow-up is inconsistent. Staff forget. Evenings and weekends go uncovered.

---

## The Solution

This workflow monitors incoming leads and triggers an AI-written, personalised
follow-up email if no response has been logged within 2 hours.

No manual intervention required. Runs 24/7.

---

## How It Works

1. **Lead captured** — form submission received via webhook
2. **Logged to Google Sheets** — lead data written to a tracking sheet
3. **Response check** — workflow checks whether the lead has been responded to
4. **AI email generated** — if unresponded after 2 hours, Groq generates a personalised follow-up
5. **Email sent** — Brevo delivers the email from the business's address
6. **Telegram alert** — owner notified so they can follow up personally if needed

---

## Stack

| Tool | Role |
|------|------|
| n8n (self-hosted) | Workflow orchestration |
| Groq (LLaMA 3) | AI email generation |
| Brevo | Email delivery |
| Google Sheets | Lead tracking and response logging |
| Telegram | Owner alerts |

---

## Use Case

- Triggers personalised follow-up within 2 hours of an uncontacted lead
- Emails personalised to the lead's name and enquiry type
- Owner receives Telegram notification for every triggered follow-up
- Designed for UK trades, hair salons, and independent restaurants

---

## Setup

### Prerequisites
- n8n instance (self-hosted or cloud)
- Groq API key (free tier works)
- Brevo account (free tier works)
- Google Sheets with service account credentials
- Telegram bot token

### Installation

1. Clone or download this repo
2. Import `missed-lead-recovery.json` into your n8n instance
3. Copy `.env.example` to `.env` and fill in your credentials
4. Configure the Google Sheet ID and column mappings in the workflow
5. Activate the workflow

See `.env.example` for all required environment variables.

---

## Project Status

✅ Built and tested
🧪 Demonstration build — fully functional, available to deploy
📍 Designed for UK small business use cases

---

## Author

**Zayd Akhtar** — AI Automation Builder
[LinkedIn](https://www.linkedin.com/in/zayd-a-03b681144/) ·
[GitHub](https://github.com/zaydakhtar)
Open to remote contracts and consulting · Based in the UK
