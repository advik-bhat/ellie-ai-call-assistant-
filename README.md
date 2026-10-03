# Ellie — AI Call Assistant 📞

> Let AI handle the call. You handle what matters.

Ellie is a prototype of an AI-powered personal call assistant designed to
answer calls on behalf of the user, understand caller intent, handle routine
conversations, identify low-priority or suspicious calls, and escalate
important conversations with concise, actionable summaries.

## 🚀 Demo

**Live Demo:** https://ellie-ai-call-assistant.netlify.app

---

## 💡 Problem

Not every phone call deserves your immediate attention.

People regularly receive delivery calls, appointment calls, sales calls,
spam calls, service calls, and important personal or professional calls.
Manually answering and screening every call is time-consuming.

Ellie explores the idea of an AI assistant that can act as a first layer
between the caller and the user.

Instead of asking:

> "Who is calling?"

Ellie aims to answer:

> "Why are they calling, can I handle it, and does the user actually need
> to know about it?"

---

## 🎯 Solution

Ellie acts as an AI call secretary that:

- Answers and screens incoming calls
- Identifies caller intent
- Classifies calls by priority and category
- Handles routine conversations
- Detects potential spam and low-priority calls
- Collects relevant information
- Escalates important calls
- Generates structured call summaries
- Produces actionable follow-up items
- Allows the user to configure how different types of calls should be handled

The core principle is:

> **The assistant handles the conversation; the user handles what matters.**

---

## ✨ Features

### 📞 Call Handling

- Interactive call simulation
- Multiple realistic call scenarios
- Natural conversational flow
- Caller intent detection
- AI identity disclosure

### 🧠 Call Classification

Calls can be categorized as:

- Urgent / Important
- Personal
- Work
- Delivery / Service
- Appointment / Scheduling
- Sales / Marketing
- Spam / Low Priority
- Unknown

### 🚨 Intelligent Escalation

Important calls can be escalated to the user with:

- Caller
- Reason for calling
- Key information
- Required action
- Priority

### 📋 Call Summaries

Each completed call can produce a structured summary containing:

- Intent
- Key information
- Decisions
- Action items
- Follow-up requirements
- Suggested next step

### ⚙️ Assistant Rules

Users can configure how Ellie handles different categories of calls,
including:

- Auto-handle
- Take a message
- Always ask the user
- Decline
- End the call

### 🔐 Privacy & Safety

The prototype includes configurable safeguards such as:

- No OTP sharing
- No address sharing
- Mandatory AI disclosure
- Escalation rules for sensitive conversations

---

## 🧪 Demo Scenarios

The prototype includes several realistic scenarios:

| Scenario | Expected Behaviour |
|---|---|
| 🏦 Bank manager | Escalate to user |
| 📦 Delivery partner | Handle routinely |
| 🛡️ Insurance salesperson | Collect information |
| 🦷 Dental clinic | Handle appointment-related conversation |
| 👤 Friend | Personal conversation |
| 🤖 Suspicious robocall | Identify as low priority / spam |

---

## 🛠️ Tech Stack

- HTML
- CSS
- JavaScript
-Netlify

The current prototype is browser-based and self-contained.

---

## 🧠 Current Implementation

This version is a functional browser prototype.

The conversational behavior and intent classification are currently
implemented using a scripted conversational engine and keyword-based
detection. This allows the complete product experience, interaction flow,
classification logic, escalation behavior, and UI to be demonstrated
without requiring a backend.

The architecture is designed to be extended with a real-time speech and
LLM pipeline.

---

## 🔮 Future Improvements

### Voice AI

Connect the assistant to real-time speech recognition and text-to-speech
to enable actual voice conversations.

### Sarvam Integration

Integrate Sarvam's speech and language APIs for:

- Speech-to-text
- Multilingual conversational understanding
- Text-to-speech
- Indian-language and code-mixed conversations

### Real Phone Calls

Connect the agent to a telephony provider so Ellie can actually answer
incoming phone calls.

### Personal Knowledge

Allow users to provide controlled information about themselves so Ellie
can answer routine questions on their behalf.

### Calendar Integration

Allow Ellie to schedule, reschedule, and confirm appointments when
authorized.

### Smarter Spam Detection

Use conversational context and model-based classification rather than
keyword-only detection.

---

## 🏗️ Product Architecture

The intended production architecture is:

```text
                 Incoming Call
                       │
                       ▼
                Speech Recognition
                       │
                       ▼
              Conversational AI
                       │
             ┌─────────┴─────────┐
             ▼                   ▼
       Intent Detection      User Rules
             │                   │
             └─────────┬─────────┘
                       ▼
                 Decision Engine
                       │
          ┌────────────┼────────────┐
          ▼            ▼            ▼
       Handle       Collect      Escalate
       Directly     Message      to User
          │            │            │
          └────────────┼────────────┘
                       ▼
                 Call Summary
                       │
                       ▼
                 User Dashboard
