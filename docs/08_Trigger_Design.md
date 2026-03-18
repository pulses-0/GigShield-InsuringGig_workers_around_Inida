# 8. Parametric Trigger Design

← [Previous](07_Trigger_System.md) | [Next](09_Risk_Engine.md)

The Parametric Trigger Design defines how real-world data is converted into deterministic, verifiable conditions that initiate insurance events.

This component ensures that all triggers are:

- objective  
- reproducible  
- reliable  
- scalable  

---

## Design Objectives

The trigger design aims to:

- ensure fairness through measurable conditions  
- avoid ambiguity in claim generation  
- minimize false positives and false negatives  
- maintain consistency across all users  

---

## Core Design Principles

### 1. Measurability
All triggers must be based on quantifiable data.

Examples:
- rainfall intensity (mm/hour)  
- AQI levels  
- temperature  

---

### 2. Objectivity
Triggers must not rely on user-reported inputs.

All decisions are based on external data sources.

---

### 3. External Verifiability
Trigger data must come from independent APIs or datasets.

This ensures:
- transparency  
- trust  
- auditability  

---

### 4. Location Specificity
Triggers are evaluated at the **delivery zone level**, not globally.

This ensures:
- relevance to the worker  
- accurate impact assessment  

---

### 5. Deterministic Behavior
Given the same input data, the system must always produce the same output.

---

## Threshold Definition

Each trigger is defined using a threshold that represents a meaningful disruption.

| Trigger Type       | Parameter            | Threshold        | Impact |
|------------------|--------------------|-----------------|--------|
| Extreme Heat     | Temperature        | ≥ 45°C          | reduced efficiency |
| Heavy Rainfall   | Rainfall Intensity | ≥ 65 mm/hour    | unsafe conditions |
| Air Pollution    | AQI                | ≥ 400           | health risk |
| Traffic          | Congestion Index   | predefined      | delays |
| Flood Alert      | Official Signal    | issued          | halt operations |

---

## Trigger Evaluation Logic

Triggers are evaluated using rule-based conditions.

### Example

IF rainfall ≥ 65 mm/hour
AND delivery_zone = affected_zone
THEN trigger event

## Multi-Source Validation

To improve accuracy, the system validates triggers using multiple data sources.

Example
IF source_1 ≥ threshold
AND source_2 ≥ threshold
THEN confirm trigger

If sources conflict:

increase uncertainty score

delay or re-validate

## Temporal Validation

To prevent false triggers caused by short spikes:

conditions must persist for a minimum duration

example: rainfall must exceed threshold for ≥ 15 minutes

 This avoids unnecessary claim generation.

## Spatial Mapping

Trigger data is mapped to delivery zones using:

geo-coordinates

pin codes

proximity to dark stores

Only users within affected zones are considered.

## Severity Classification

Each event is assigned a severity level based on how much the threshold is exceeded.

Level	Condition
Moderate	threshold to +10%
High	+10% to +25%
Critical	> +25%

Severity can influence:

payout priority

system alerts

## Trigger Deduplication

To prevent redundant events:

IF same_trigger_type
AND same_zone
AND within_time_window
THEN merge events

This ensures:

cleaner data

accurate payouts

reduced system load

## Trigger Lifecycle

Each trigger follows a defined lifecycle:

Detection

Validation

Event Creation

Notification to Claims Engine

Resolution

## Edge Case Handling

The system handles:

sudden data spikes → smoothing applied

missing data → fallback sources used

conflicting data → re-validation triggered

## Key Characteristics

deterministic and rule-based

highly scalable across cities

resistant to noise and false signals

transparent and auditable

```text

Why This Matters

This design ensures that:

every payout is justified

no manual intervention is needed

the system remains fair and consistent

Without proper trigger design:

false claims increase

system trust decreases

financial sustainability is affected
