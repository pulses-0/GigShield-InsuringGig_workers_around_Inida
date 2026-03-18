# 6. System Workflow

GigShield operates as a fully automated, event-driven system that continuously monitors real-world conditions and responds in real time.

Instead of relying on user actions, the platform works as a **background protection layer** for delivery partners.

---

## End-to-End Flow


User Onboards
→ Risk Profile Generated
→ Weekly Premium Calculated
→ Policy Activated
→ Real-Time Monitoring Starts
→ Disruption Detected
→ Claim Auto-Created
→ Fraud Validation
→ Payout Processed
→ User Notified


## Workflow Overview

The workflow can be divided into three major phases:

a. Setup Phase

b. Monitoring Phase

c. Event & Payout Phase

Each phase plays a critical role in ensuring seamless and automated income protection.

## a. Setup Phase (Before Any Disruption)

This phase prepares the user for coverage and ensures that the system has all necessary data to operate effectively.

# Onboarding

The delivery partner registers on the platform and provides essential details:

delivery platform (e.g., Zepto, Blinkit)

delivery zone (pin code / location)

working pattern or activity level

This information is used to create a verified worker profile.

# Risk Profiling

The system evaluates the worker’s environment using:

historical weather data

AQI trends

disruption frequency in the delivery zone

Based on this, a risk score (1–100) is assigned.

# Premium Calculation

The weekly premium is calculated using:

risk score

selected coverage level

estimated earnings

This ensures that pricing is fair and reflects actual exposure.

# Policy Activation

The worker activates a weekly policy.

At this stage:

coverage becomes active

the user is eligible for payouts

the system begins monitoring conditions

## Monitoring Phase (Continuous Background Process)

Once a policy is active, GigShield runs continuously in the background.

The system monitors multiple external data sources in real time:

 weather data (temperature, rainfall)

 air quality (AQI levels)

 traffic conditions

 public alerts (curfews, strikes)

 Data Processing

Incoming data is:

fetched periodically from APIs

mapped to delivery zones

evaluated against predefined thresholds

This phase ensures that the system is always aware of current conditions.

## Event & Payout Phase (When Disruption Occurs)

This phase is triggered automatically when a disruption is detected.

# Trigger Detection

If any monitored parameter crosses a threshold, a Disruption Event is created.

Examples:

rainfall ≥ 65 mm/hour

AQI ≥ 400

official flood alert

These conditions indicate that normal delivery operations are impacted.

# Automatic Claim Creation
 
Once a disruption event is detected:

the system identifies all workers with active policies

filters those within the affected delivery zone

→ claims are created automatically

No manual input is required from the user.

# Fraud Validation

Before approval, each claim undergoes validation:

GPS location verification

activity status check

duplicate claim detection

anomaly detection

This ensures fairness and prevents misuse.

# Payout Processing

After validation:

payout amount is calculated

processed via mock UPI / Razorpay

Typical processing time: within minutes

# User Notification

The user receives real-time updates:

disruption alert

claim status (created, approved, paid)

payout confirmation

## Key Highlights

Zero User Effort → everything is automatic

Real-Time Processing → reacts instantly to events

Zone-Based Logic → hyperlocal decision making

Fast Payouts → aligned with gig worker needs

## Why This Workflow Matters

Traditional systems require:

manual claims

long processing times

complex verification

GigShield replaces this with:

automated detection

instant validation

immediate payouts

# This makes the system fast, fair, and scalable for gig workers.
