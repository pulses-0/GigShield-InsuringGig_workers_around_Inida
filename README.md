# GigShield

### AI-Powered Income Protection for Q-Commerce Delivery Partners

---
## Demo Video

Watch the demo: https://youtube.com/shorts/cAXEJE4BSSY?feature=share


## The Problem

Quick commerce platforms like Blinkit, Zepto, and Swiggy Instamart operate on ultra-fast delivery cycles (10–30 minutes), where delivery partners earn per completed order.

This creates a critical vulnerability:

**If they can’t work, they don’t earn.**

### Real-World Situations

* **Chennai (Monsoon Season):** Sudden heavy rainfall floods roads, making deliveries impossible for 2–3 hours
* **Delhi (Winter):** AQI crosses 400, Very heavy smog, reducing rider availability and order flow
* **Bangalore (Peak Hours):** Severe traffic congestion delays deliveries beyond SLA limits
* **Hyderabad:** Fuel shortages, Railway crossing malfunction, temporarily halt delivery operations

### Impact

* ₹400–₹800 lost in a single day
* Up to 20–30% monthly income loss
* No system currently protects short-duration income disruption

Traditional insurance models are not suitable because they are slow, manual, and focused on accidents rather than income loss.

---

## Market Opportunity

* Over 5 million gig delivery workers in India
* Rapid expansion of quick-commerce platforms
* Increasing dependency on gig-based income

Despite this scale, there is **no real-time income protection system**.

GigShield introduces a new category: **parametric micro-insurance for gig workers**.

---

## Our Solution — GigShield

GigShield is a parametric, AI-powered insurance platform that protects gig workers from short-term income loss.

Instead of requiring users to file claims:

* The system continuously monitors real-world data
* Detects disruptions automatically
* Verifies them using trusted external sources
* Triggers instant payouts

This removes friction and ensures timely financial support.

---

## How It Works

### High-Level Flow

User registers → Risk score generated → Weekly policy activated
→ Real-time monitoring → Disruption detected
→ Claim auto-created → Fraud checked → Instant payout

---

## Detailed Workflow

### 1. Onboarding

User provides delivery zone, platform (Blinkit, Zepto, etc.), and working hours

---

### 2. Risk Profiling

The system builds a **location-specific risk profile** using:

* Historical rainfall data (e.g., IMD datasets)
* AQI trends (OpenAQ)
* Traffic congestion patterns

**Example:**
A rider in Chennai may have a higher risk score during October–December due to monsoon flooding patterns.

---

### 3. Premium Calculation

Premium is dynamically calculated based on:

* Risk score
* Coverage level
* Expected disruption frequency

**Example:**

* Low-risk zone → ₹50/week
* High-risk zone → ₹120/week

---

### 4. Policy Activation

User activates a weekly plan aligned with their earning cycle.

---

### 5. Continuous Monitoring

The system ingests real-time data streams:

* Weather APIs (rainfall, temperature)
* AQI APIs
* Traffic APIs
* Public alerts (simulated or government feeds)

This runs as an **event-driven pipeline**.

---

### 6. Trigger Detection

When thresholds are crossed, a disruption event is generated.

**Examples:**

* Rainfall ≥ 65 mm/hr (cloudburst-like conditions)
* AQI ≥ 400 (hazardous category)
* Traffic congestion index above threshold

---

### 7. Automatic Claim Creation

The system identifies:

* Active users
* Within affected radius (2–5 km)

Claims are generated automatically.

**Example:**
If heavy rain hits Velachery, only riders active in that zone receive claims.

---

### 8. Fraud Validation

Each claim is validated using multi-layer checks:

* GPS location vs disruption zone
* Recent activity logs
* Historical behavior patterns

---

### 9. Instant Payout

Approved claims are processed via Razorpay (test mode).

**Example:**
A rider earning ₹120/hour, inactive for 2 hours during disruption:

Payout = 120 × 2 × 0.6 = ₹144

---

### 10. Notification

Users receive real-time updates on:

* Disruption detection
* Claim approval
* Payout completion

---

## End-to-End Example Scenario

**Scenario: Chennai Evening Peak (6–9 PM)**

* Heavy rainfall detected: 72 mm/hr
* System identifies affected zones (Adyar, Velachery)
* 120 active riders detected in region
* Claims auto-generated

Fraud validation checks:

* GPS confirms presence in zone
* Rider activity logs show recent deliveries

Result:

* Average payout: ₹150–₹300 per rider
* Total processing time: under 2 minutes

---

## AI & Risk Engine

### Inputs

* Historical weather datasets
* AQI time-series data
* Traffic congestion patterns
* User activity frequency

### Outputs

* Risk score (1–100)
* Expected disruption probability

### Models Used

* Random Forest for risk prediction
* Gradient Boosting for premium optimization
* Isolation Forest for anomaly detection

---

## Advanced Fraud Detection

GigShield implements a layered fraud detection pipeline:

### Behavioral Analysis

* Detects sudden inactivity patterns aligned with triggers
* Flags repeated claims at identical timestamps

### Geo-Validation

* Cross-verifies GPS with disruption zones
* Detects spoofed or static locations

### Cross-User Correlation

* Identifies clusters of suspicious claims
* Detects coordinated fraud attempts

### AI-Based Anomaly Detection

* Isolation Forest assigns anomaly scores
* High-risk claims are flagged or rejected

---

## Insurance Model

### Coverage Options

* Basic → 40%
* Standard → 60%
* Premium → 80%

### Payout Formula

Payout = Hourly Income × Disruption Duration × Coverage %

---

## What Triggers a Payout

### Weather

* Heavy rainfall
* Flood alerts
* Extreme heat

### Environment

* AQI ≥ 400

### Infrastructure

* Traffic congestion
* Road closures

### Socio-Economic

* Fuel shortages
* Strikes / curfews
* Platform outages

---

## System Architecture

### Data Layer

* External APIs (weather, AQI, traffic)

### Processing Layer

* Event-driven trigger engine
* AI risk scoring system
* Fraud detection module

### Action Layer

* Claims engine
* Payment gateway integration
* Notification system

---

## External Integrations

* OpenWeatherMap / IMD → weather data
* OpenAQ → air quality
* Google Maps API → traffic insights
* Public alert systems → disruption signals
* Razorpay → instant payouts (test environment)

---

## Tech Stack

| Layer         | Tech                  |
| ------------- | --------------------- |
| Frontend      | React / Next.js       |
| Backend       | FastAPI / Node.js     |
| Database      | PostgreSQL            |
| AI/ML         | Python (scikit-learn) |
| Payments      | Razorpay (Test Mode)  |
| Notifications | Firebase              |

---

## Performance Metrics (Simulated)

* Trigger detection latency: < 60 seconds
* Claim processing time: < 2 minutes
* Fraud detection accuracy: ~92%
* False positive rate: < 5%

---

## Key Features

* Fully automated claim lifecycle
* AI-driven dynamic pricing
* Hyperlocal disruption detection
* Real-time event processing
* Instant payouts
* Advanced fraud detection

---

## Why GigShield Stands Out

* Addresses a real and underserved problem
* Built specifically for gig economy workers
* Combines parametric insurance with real-time data systems
* Eliminates manual claims entirely
* Designed for scalability and real-world deployment

---

## Future Scope

* Integration with delivery platform APIs (Blinkit, Zepto)
* Real-time rider telemetry
* Reinforcement learning for adaptive pricing
* Blockchain-based claim audit trails
* Expansion to other gig sectors (ride-sharing, freelancing)

---

## Demo Video

--video link--

---

## Repo Structure

```
docs/        → detailed documentation  
diagram/    →  architecture + workflows    
video/       → demo link  
```

---

## Team

* Usham Roy - Team Lead
* Venumadhav S
* N V Jatin Pochiraju
* Riddhi Mehrotra
* Palash Rai

---

```text

GigShield is designed as a real-time financial safety system for gig workers, combining data-driven intelligence with automated insurance execution to protect income in uncertain environments.

---
