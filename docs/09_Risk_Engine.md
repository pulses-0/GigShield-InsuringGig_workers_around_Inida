# 9. AI Risk & Premium Engine

The AI Risk & Premium Engine is responsible for estimating the likelihood of disruptions affecting a delivery partner and calculating a fair weekly insurance premium.

This component ensures that pricing is:

- data-driven  
- dynamic  
- personalized  
- scalable  

---

## Objectives

The Risk Engine is designed to:

- quantify disruption risk for each worker  
- enable fair and adaptive pricing  
- account for hyperlocal conditions  
- continuously update based on new data  

---

## Risk Factors

The system evaluates multiple categories of inputs:

---

### Environmental Factors
- rainfall patterns  
- extreme heat frequency  
- flood-prone areas  

---

### Air Quality Factors
- AQI trends  
- frequency of severe pollution events  

---

### Urban Mobility Factors
- traffic congestion patterns  
- road closure frequency  

---

### Socio-Economic Factors
- strikes and curfews  
- fuel shortages  
- zone-level disruptions  

---

### Operational Factors
- delivery zone characteristics  
- proximity to dark stores  
- historical delivery disruptions  

---

## Data Inputs

The engine uses a combination of:

- historical data (1–2 years) → baseline risk  
- recent data (7–14 days) → short-term trends  
- forecast data → predictive adjustments  

All data is mapped to delivery zones before processing.

---

## Risk Score Calculation

Each user is assigned a **risk score between 1 and 100**:

- 1 → minimal risk  
- 100 → extreme risk  

### Example Formula

Risk Score =
(w1 × Weather Risk) +
(w2 × AQI Risk) +
(w3 × Traffic Risk) +
(w4 × Socio-Economic Risk)

### Risk Tier Classification

To simplify interpretation, scores are grouped:

Tier	Score Range
Low	1 – 25
Medium	26 – 50
High	51 – 75
Critical	76 – 100

## Machine Learning Models

The system can use:

Random Forest

Gradient Boosting

Logistic Regression

For anomaly detection:

Isolation Forest

These models learn relationships between:

external conditions

disruption events

delivery performance

## Premium Calculation

Premiums are calculated based on:

risk score

coverage level

estimated weekly income

Formula
Weekly Premium =
Base Rate × Risk Multiplier × Coverage Multiplier

## Constraints

premium range: ₹29 – ₹199

recalculated weekly

must remain affordable for users

## Dynamic Adjustment

At the start of each week:

risk score is updated

premium is recalculated

user is notified

This ensures pricing adapts to:

seasonal changes

recent disruptions

forecast conditions

## Explainability

To maintain trust:

users can see their risk score

premium breakdown is shown

changes are explained clearly

## Key Characteristics

hyperlocal risk modeling

adaptive pricing

AI-assisted decision making

transparent and explainable

## Example

A delivery partner in Chennai:

high rainfall frequency

frequent flooding

→ Risk Score = 72 (High)

If:

Base rate = ₹50

Risk multiplier = 1.5

Coverage multiplier = 1.2

→ Premium ≈ ₹90

```text
Why This Matters

Without risk-based pricing:

low-risk users overpay

high-risk users exploit system

sustainability breaks

This engine ensures:

fairness

scalability

long-term viability
