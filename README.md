# Project
Guidewire Devtrails Project
# GigShield

### AI-Powered Income Protection for Q-Commerce Delivery Partners

---

## The Problem

Quick Commerce platforms like Blinkit and Zepto rely on delivery partners who work in tight 10–30 minute delivery windows. Their income depends entirely on how many deliveries they complete.

The problem is simple but serious:

> If they can’t work, they don’t earn.

And a lot of things can stop them from working:

* heavy rain
* extreme heat
* poor air quality
* traffic congestion
* fuel shortages
* strikes or curfews

Even a short disruption during peak hours can cause:

* ₹400–₹800 loss in a single day
* up to **20–30% loss in monthly income**

There is currently **no system that protects this kind of income loss**.

---

## Our Solution — GigShield

GigShield is a **parametric insurance platform** designed specifically for gig workers.

Instead of asking users to file claims:

* the system continuously monitors real-world conditions
* detects disruptions automatically
* verifies them using external data
* and **pays users instantly without any manual effort**

No paperwork. No delays. No friction.

---

## How the System Works

At a high level, GigShield runs as a continuous loop:

```text
User registers → gets risk profile → buys weekly policy  
→ system monitors real-world data  
→ disruption detected → claim auto-created  
→ fraud checked → payout processed → user notified
```

---

## Detailed Workflow

### Step 1: Onboarding

The delivery partner signs up and provides basic details like delivery zone, platform, and activity level.

---

### Step 2: Risk Profiling

The system analyzes the worker’s location and historical data (weather, AQI, disruptions) to generate a **risk score (1–100)**.

---

### Step 3: Premium Calculation

Based on the risk score and selected coverage level, a **weekly premium** is calculated.

---

### Step 4: Policy Activation

The user activates a weekly plan aligned with their earning cycle.

---

### Step 5: Continuous Monitoring

The system continuously tracks:

* weather conditions
* air quality
* traffic
* public alerts

---

### Step 6: Trigger Detection

If any parameter crosses a threshold (e.g., heavy rain, AQI spike), a **disruption event** is created.

---

### Step 7: Automatic Claim Creation

All affected users in that delivery zone automatically get a claim — no action needed.

---

### Step 8: Fraud Validation

The system checks:

* GPS location
* activity status
* duplicate claims
* abnormal patterns

---

### Step 9: Instant Payout

Approved claims are processed instantly using mock UPI/Razorpay.

---

### Step 10: User Notification

The user gets real-time updates about:

* disruption events
* claim status
* payout confirmation

---

## Key Features

### a. Fully Automated (Zero-Touch)

No manual claims, no documents — everything is system-driven.

### b. AI-Based Risk Pricing

Premiums are calculated dynamically based on real-world risk.

### c. Real-Time Trigger Engine

The system continuously monitors external data and reacts instantly.

### d. Hyperlocal Intelligence

Everything is evaluated at the delivery zone level (2–5 km radius).

### e. Instant Payouts

Money is processed within minutes after validation.

### f. Fraud Detection

Combination of:

* rule-based checks
* AI anomaly detection

---

## Who Is This For?

### Primary Users

* Full-time delivery partners
* Highly dependent on daily income

### Also Covers

* Part-time workers
* Multi-platform riders
* New riders
* Night-shift workers

---

## What Triggers a Payout?

GigShield uses real-world data to detect disruptions:

### Weather

* Extreme Heat (≥ 45°C)
* Heavy Rainfall (≥ 65 mm/hr)
* Flood Alerts

### Environment

* Severe Pollution (AQI ≥ 400)

### Infrastructure

* Traffic congestion
* road closures

### Social / Economic

* fuel shortages
* strikes / curfews
* platform outages

---

## System Architecture

![Architecture](README_assets/architecture.png)

The system is built as a modular architecture with:

* PWA frontend
* backend API layer
* trigger engine
* claims engine
* fraud detection
* AI risk engine
* payout system

---

## AI & Risk Engine

* assigns risk score (1–100)
* uses historical + real-time data
* applies ML models like:

  * Random Forest
  * Gradient Boosting
  * Isolation Forest

Premiums are recalculated every week based on updated risk.

---

## Insurance Model

GigShield uses a **weekly coverage model**.

### Coverage Options

* Basic → 40% protection
* Standard → 60%
* Premium → 80%

### Payout Calculation

```text
Payout = Hourly Income × Disruption Duration × Coverage %
```

---

## Fraud Detection

To keep the system fair:

* verifies user location (GPS)
* checks if user was active
* prevents duplicate claims
* detects abnormal behavior

Each claim gets a fraud score before approval.

---

## External Integrations

* Weather APIs
* Air Quality APIs (OpenAQ)
* Traffic APIs
* Public alerts (mock)
* Razorpay (test mode)

---

## 🛠 Tech Stack

| Layer         | Tech                  |
| ------------- | --------------------- |
| Frontend      | React / Next.js       |
| Backend       | FastAPI / Node.js     |
| Database      | PostgreSQL            |
| AI/ML         | Python (scikit-learn) |
| Payments      | Razorpay (Test Mode)  |
| Notifications | Firebase              |

---

## System Highlights

* Trigger detection in **< 60 seconds**
* Payouts in **< 2 minutes**
* Scalable to **100k+ users**
* Fully automated workflow

---

## Why This Is Different

* Built specifically for gig workers
* Focuses on **income loss**, not accidents
* No manual claim process
* Real-time, data-driven system

---

## Demo Video

(Add your link here)

---

## Repo Structure

```bash
docs/        → detailed documentation  
diagrams/    → architecture + workflow  
ui/          → mockups  
video/       → demo link  
```

---

## Detailed Documentation

Full system design available in `/docs` folder.

---

## Team

* Palash Rai
* (Add teammates)

---
