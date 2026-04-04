---
title: "JOCKO: AI Accountability Coach"
date: 2026-04-04
categories: [electronics]
tags: [Python, AI, Vibe Code, Accountability Coach, Fitness, Telegram, Garmin]
status: "Complete"
image: "assets/project_photos/Jocko/discipline_equals_freedom.png"
excerpt: "An agentic accountability system that combines data and AI coaching with financial disincentives to reach goals. Named after Jocko Willink, it pulls fitness data from Garmin, generates context-aware coaching messages, and sends PayPal payments to a nominated recipient if weekly goals are missed."
---

## Disclaimer

This project is an independent tool inspired by Jocko Willink's and Ryan Holidays philosophies. It is not affiliated with, endorsed by, or associated with them personally or with their companies.

## Overview

**Put your money where your mouth is.**

JOCKO is an automated accountability system that communicates through Telegram and is designed for people tired of breaking promises to themselves. It operates on a simple principle: **you pre-commit to specific actions, and you pay a penalty if you fail.** The system removes ambiguity by creating concrete daily commitments, tracking them automatically via Garmin Connect, assessing their veracity, and enforcing financial consequences through PayPal if you don't show up.

The system also integrates daily mindfulness by delivering a passage from *The Daily Stoic* by Ryan Holiday every morning as part of the wake-up routine.

---

![Alt text](assets/project_photos/Jocko/Jocko_automated_accountability_system.png)

---

## Technical Approach

The architecture is built in six distinct layers, each with a single responsibility:

1. **Data Ingestion** — pulls activity data from Garmin Connect (workouts, heart rate, body battery, sleep, steps)
2. **Memory** — SQLite database storing goals, training history, daily commitments, and conversation context
3. **Decision Engine** — Analyzes metrics and trends to determine goal compliance and coaching interventions
4. **Language Layer** — Generates context-aware coaching messages via OpenAI GPT-4o, shaped by intensity setting and live data
5. **Accountability Layer** — Automatically sends pre-committed PayPal funds to a nominated recipient if weekly goals are missed
6. **Communication Layer** — Delivers coaching via Telegram with two-way conversation and proactive prompting throughout the day

### Data Veracity

The system validates workout data to prevent gaming. Activities are analyzed for heart rate consistency, duration vs. effort, and historical patterns. Suspicious data is flagged and the coach factors this into accountability conversations — you cannot log a 5-minute "run" with no heart rate elevation and have it count.

---

## Execution

### The Daily Commitment Loop

The system runs on a structured daily rhythm:

**Evening Planning:** Each night, the coach asks for tomorrow's wake-up time and gym time. The phrasing varies naturally through AI generation, shaped by your intensity setting — from warm and supportive at low intensity to blunt and confrontational at high intensity.

**Morning Execution:** At your nominated wake-up time, the coach fires a wake-up message that includes that day's passage from *The Daily Stoic* — a philosophical prompt to frame your mindset. A `WAKE_UP` trigger token allows Tasker on Android to override silent mode and fire a full-volume alarm.

**Accountability Checkpoints:** At your committed gym time + 120 minutes, the system checks your Garmin data. If no session is logged within the expected window, the coach initiates contact based on your frequency and intensity settings. Jocko will also stay on top of your progress throughout the week and get up you if you're falling behind.

**Weekly Enforcement:** At week's end, the system evaluates goal compliance. If you missed your targets, a PayPal payment is automatically sent to your nominated recipient. A weekly report is generated to summarize your performance and highlight areas for improvement.

### Intensity and Frequency Controls

Two independent controls allow fine-tuning of the coaching experience:

| Intensity (1-10) | Character |
|---|---|
| 1-3 | Warm, conversational — like a supportive friend checking in |
| 4-6 | Direct and businesslike — always to the point |
| 7-9 | Blunt, impatient, occasionally cutting |
| 10 | Full Jocko Willink. Terse, aggressive, creative insults |

| Frequency (1-10) | Behaviour |
|---|---|
| 1-3 | Wake-up + evening planning only |
| 4-6 | Above + gym check-in + evening warning if goal at risk |
| 7-9 | Above + midday nudge |
| 10 | Above + breach alerts as they occur |

### Conversational Context

You can message the bot at any time. It responds with full awareness of your training data, recent commitments, conversation history, and configured tone. The coach remembers what you said and holds you to it.

---

## Specifications

| Parameter | Value |
|-----------|-------|
| Language | Python 3.10+ |
| Database | SQLite |
| AI Model | OpenAI GPT-4o |
| Fitness Data | Garmin Connect API |
| Communication | Telegram Bot API |
| Payments | PayPal Payouts API |
| Scheduling | APScheduler |
| Deployment | systemd service on Linux VPS |

---

## Project Files

- Read below before accessing the [GitHub Repository](https://github.com/mgreenhough/JOCKO)
- [Installation Guide](ai-coach/README.md)

## LEGAL NOTICE

This repository contains copyrighted material from "The Daily Stoic" by Ryan Holiday and Stephen Hanselman.

# Access Restrictions: 
This content is intended solely for individuals who have purchased a legitimate copy of "The Daily Stoic" book. By accessing this repository, you confirm that you own a legally obtained copy of the book.

Fair Use Notice: The material in this repository is provided for personal educational and reference purposes only. This falls under fair use for:

Personal study and reflection
Educational purposes
Commentary and discussion
Prohibited Uses:

Redistribution or resale of this content
Commercial use without authorization
Sharing with individuals who do not own the book
If you have not purchased "The Daily Stoic," please do not access this repository. Support the authors by purchasing the book from authorized retailers.

## Warning

**This project is 100% vibe-coded. It is not robust, not complete, and not supported or maintained to any production standard.**

In the interest of efficiency and achieving an MVP as fast as possible, quality, robustness, and long-term maintainability were knowingly deprioritised.

This is an experimental, exploratory build — not a polished or supported product.
You are free to use it under the terms of the MIT License, but do so at your own risk.

That said, contributions, issues, and improvements are welcome. If you spot a problem or have an idea, feel free to open an issue or submit a PR — I’ll address things where time and interest permit, but no guarantees.

---