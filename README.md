# Sereni – AI-Driven Sentiment Analysis Chatbot
Visit Here : https://empathy-bot--tanishkabarbate.replit.app/
Sereni is an AI-powered web application designed to provide supportive and empathetic responses based on the emotional tone of user messages.

The system uses sentiment analysis and a rule-based risk detection layer to identify emotional distress and possible crisis-related language. Based on the detected emotional state, Sereni provides supportive responses, grounding techniques, and appropriate escalation guidance.

> **Disclaimer:** Sereni is an academic demonstration project. It is not a replacement for a qualified mental-health professional, emergency service, or medical advice.

---

## 🌿 Project Overview

Sereni combines Artificial Intelligence, Natural Language Processing, web development, security, and database technologies into a single application.

The application:

- Analyzes user messages in real time
- Detects positive, neutral, and negative sentiment
- Estimates emotional distress levels
- Detects crisis and suicidal-ideation-related phrases
- Provides empathetic chatbot responses
- Offers the 5-4-3-2-1 grounding technique for moderate distress
- Provides emergency support information for high-risk situations
- Stores chat history
- Tracks emotional trends and grounding usage
- Uses authentication and password hashing
- Includes CSRF protection and input sanitization
- Provides a responsive glassmorphism-based interface

---

## ✨ Features

### 🤖 AI & NLP

- VADER-based sentiment analysis
- Text preprocessing and cleaning
- Tokenization
- Feature extraction
- Sentiment scoring
- Confidence score simulation
- Modular ML pipeline
- Designed so VADER can later be replaced with BERT or another ML model

### 🛡️ Risk Detection

Sereni uses a rule-based crisis detection system with multiple risk levels:

- **Low Risk** – normal emotional conversation
- **Moderate Risk** – signs of significant emotional distress
- **High Risk** – possible crisis or suicidal ideation
- **Protective Phrases** – language indicating safety, support, or coping

The system returns structured information including:

- Sentiment score
- Sentiment label
- Risk level
- Confidence score
- Detected indicators

---

## 🧘 Grounding Support

For moderate distress, Sereni can provide a guided **5-4-3-2-1 grounding exercise**.

The user is guided through:

1. 5 things you can see
2. 4 things you can touch
3. 3 things you can hear
4. 2 things you can smell
5. 1 thing you can taste

The grounding session is managed separately for each user session.

---

## 🚨 Emergency Support

Sereni provides calm and accessible emergency support options.

### Emergency Call

**022 2754 6669**

### Emergency Text

**85258**

The buttons do not automatically call or redirect the user. Instead, the information is softly revealed when the user clicks the corresponding button.

> If you are in immediate danger, contact your local emergency services.

---

## 💬 Chat History

The application includes a chat history section on the left side of the interface.

Users can:

- View previous conversations
- Start a new conversation
- Continue previous conversations
- See conversation timestamps
- Keep conversations organized

---

## 🎨 User Interface

Sereni uses a calming dark glassmorphism design.

### Design Principles

- Deep navy background
- Soft lavender highlights
- Calm teal success states
- Soft red emergency controls
- Glass-effect cards
- Rounded components
- Subtle shadows
- Smooth animations
- Minimal scrollbar
- Responsive desktop and mobile layout

The interface also includes subtle decorative elements such as:

- Crescent moon
- Sparkle stars
- Planetary ring
- Floating background circles

The design intentionally avoids aggressive colors and visual clutter.

---

## 🏗️ System Architecture

```text
                    ┌─────────────────────┐
                    │       User          │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Frontend UI       │
                    │ HTML/CSS/JavaScript │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Flask Backend    │
                    └──────────┬──────────┘
                               │
              ┌────────────────┼────────────────┐
              ▼                ▼                ▼
       ┌────────────┐   ┌─────────────┐  ┌─────────────┐
       │ ML Pipeline│   │Risk Classifier│ │Grounding    │
       │            │   │              │  │Engine       │
       └─────┬──────┘   └──────┬───────┘  └─────────────┘
             │                 │
             └────────┬────────┘
                      ▼
              ┌───────────────┐
              │ Response      │
              │ Generation    │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │   Database    │
              │ SQLite / ORM  │
              └───────────────┘

