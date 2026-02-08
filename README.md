# AI Appointment / Cold-Call Booking Agent

## 🧠 Overview

This project is an AI-powered appointment booking and outreach agent built using **n8n**, OpenAI, and LinkedIn tools.

It automates the process of:
- Understanding user requests
- Collecting contact information
- Generating personalized outreach messages
- Initiating calls or automated scheduling

This workflow demonstrates how AI can assist in coordination tasks (like appointment booking or lead outreach), reducing manual steps and speeding up communication.

---

## 🚨 Problem

Manual appointment booking and outreach (cold calls, emails) is:
- Time-consuming
- Repetitive
- Inefficient at scale

Particularly in healthcare or service coordination, automation can reduce friction and improve timely access.

This project explores how **AI + workflow automation** can streamline those processes.

---

## 💡 Solution

This solution uses:

1. **n8n workflow** to orchestrate steps
2. **OpenAI** to interpret user intent and generate contextual text
3. **LinkedIn + Sales Navigator** data to extract contact leads
4. **Cold-call or scheduling logic** (simulated in workflow)

The workflow:
- Receives a trigger (Webhook, form, manual start)
- Extracts user request (e.g., “Book an appointment with a dentist next week”)
- Generates a personalized outreach message
- Optionally connects to phone/call logic (via template)

---

## ⚙️ Tech Stack

| Layer | Tool |
|-------|------|
| Orchestration | n8n |
| AI Language Model | OpenAI API |
| Lead / Contact Data | LinkedIn + Sales Navigator |
| Trigger | Webhook or Form submit |
| Optional | Phone / SMS API (Twilio etc.) |

---Perfect. I’ll write this like you’re explaining to judges clearly and professionally.

You can copy-paste this into your README.md.

---

# 🚀 How to Execute the Workflow

This project contains an exported n8n workflow (`workflow.json`) that runs an AI-powered calling/appointment automation system.

The workflow is designed to run locally using Docker.

---

## 🧩 Requirements

Before running the workflow, make sure you have:

* Docker Desktop installed
  👉 [https://www.docker.com/products/docker-desktop/](https://www.docker.com/products/docker-desktop/)
* An OpenAI API key (if the workflow uses OpenAI)
* Any required external service credentials (e.g., Twilio, etc.)

---

## 🛠 Step 1 — Run n8n Locally

Open your terminal and run:

```bash
docker run -it --rm \
-p 5678:5678 \
-e N8N_BASIC_AUTH_ACTIVE=true \
-e N8N_BASIC_AUTH_USER=admin \
-e N8N_BASIC_AUTH_PASSWORD=password \
n8nio/n8n
```

Then open your browser and go to:

```
http://localhost:5678
```

Login credentials:

* Username: `admin`
* Password: `password`

---

## 📥 Step 2 — Import the Workflow

1. Click **"Import from File"**
2. Upload the provided `workflow.json` file from this repository
3. The workflow will appear in your workspace

---

## 🔑 Step 3 — Configure Credentials

Before running the workflow:

1. Open each node that requires credentials (e.g., OpenAI, Twilio)
2. Add your personal API keys
3. Save the workflow

⚠️ The workflow will not execute properly without valid credentials.

---

## ▶️ Step 4 — Execute the Workflow

You can:

* Click **"Execute Workflow"** manually
  OR
* Trigger it using the configured trigger (Webhook, Schedule, etc.)



---

## 🏗 Architecture Overview

This workflow:

1. Retrieves contact data
2. Uses OpenAI to generate conversational responses
3. Initiates automated call logic
4. Handles appointment scheduling
5. Logs interaction results

The system is modular and can be extended to support:

* Multi-language calls
* SMS fallback
* CRM integration
* Appointment confirmation tracking

---





