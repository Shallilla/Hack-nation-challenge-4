# Hack-nation-challenge-4
# AI Appointment Booking Agent

## 🧠 Overview

This project is an AI-powered appointment booking agent built using n8n.

The system automates the process of scheduling medical appointments by:
- Understanding user requests
- Extracting appointment details using AI
- Scheduling the appointment
- Sending confirmation

The goal is to simplify healthcare access by reducing manual coordination and phone calls.

---

## 🚨 Problem

Booking medical appointments can be slow and inefficient.  
Patients often need to call facilities manually, wait, and repeat information multiple times.

This project explores how AI agents can automate and streamline this process.

---

## 💡 Solution

This AI agent uses workflow automation and language models to:

1. Receive a booking request
2. Extract structured information (date, time, type of appointment)
3. Schedule the appointment
4. Confirm the booking

---

## ⚙️ Tech Stack

- n8n (workflow orchestration)
- OpenAI API (intent understanding & extraction)
- Google Calendar API (appointment scheduling)
- Webhook trigger (user input)

---

## 🏗️ Architecture

Workflow structure:

Webhook → OpenAI (Intent Extraction) → Parse Data → Google Calendar → Confirmation

---

## 🎥 Demo

Demo Video: [Add your video link here]

---

## 📂 Files

- `workflow.json` → Exported n8n workflow
- `architecture.png` → System diagram

---

## 🚀 How It Works

Example user input:

"Book a dentist appointment tomorrow at 3pm for cleaning."

The AI extracts:

{
  "appointment_type": "dentist",
  "date": "YYYY-MM-DD",
  "time": "15:00"
}

The workflow then creates the calendar event and sends confirmation.

---

## 🌍 Impact

This project demonstrates how AI agents can automate healthcare coordination and reduce friction in accessing care.

It can be expanded to support:
- Real phone calls (Twilio)
- SMS confirmations
- Hospital system integrations
- Multi-language support
