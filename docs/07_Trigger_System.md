# 7. Disruption Trigger System

← [Previous](06_System_Workflow.md) | [Next](08_Trigger_Design.md)

The Disruption Trigger System is the core component responsible for detecting real-world conditions that impact delivery operations.

It continuously monitors external data sources and identifies events that can reduce or halt a delivery partner’s ability to earn.

---

## Objective

The primary goal of the Trigger System is to:

- detect disruptions in real time  
- convert external conditions into system events  
- initiate automated insurance workflows  
- ensure objective and data-driven decision making  

---

## How the Trigger System Works

The system operates in a continuous loop:

Fetch External Data
→ Map to Delivery Zone
→ Evaluate Thresholds
→ Detect Condition Breach
→ Generate Disruption Event
→ Notify Claims Engine

## Trigger Categories

Disruptions are classified into multiple categories based on their nature and impact.

### 1. Weather-Based Triggers

These represent environmental conditions that directly affect delivery feasibility.

Examples:

Extreme Heat
Condition: Temperature ≥ 45°C
Impact: reduced rider efficiency, health risk

Heavy Rainfall
Condition: Rainfall ≥ 65 mm/hour
Impact: waterlogging, slower deliveries

Flooding
Condition: official flood alert
Impact: complete halt of operations

### 2. Environmental Triggers

These capture atmospheric conditions that affect outdoor work.

Examples:

Severe Air Pollution
Condition: AQI ≥ 400
Impact: unsafe working conditions, reduced activity

### 3. Urban / Infrastructure Triggers

These represent disruptions in city mobility.

Examples:

Traffic Congestion
Condition: congestion index above threshold
Impact: delayed deliveries, fewer orders

Road Closures
Condition: verified closure events
Impact: route disruption

### 4. Socio-Economic Triggers

These capture disruptions caused by social or economic factors.

Examples:

Fuel Shortages
Condition: abnormal fuel availability / long queues
Impact: reduced mobility

Strikes / Curfews
Condition: official government alerts
Impact: restricted movement

Platform Outages
Condition: service downtime
Impact: no order allocation

## Trigger Evaluation Logic

Each trigger is defined using a clear, measurable condition.

Example
IF rainfall ≥ 65 mm/hour
AND delivery_zone = affected_zone
THEN create Disruption Event

## Data Sources

The Trigger System integrates with external APIs such as:

weather APIs (temperature, rainfall)

air quality APIs (AQI levels)

traffic data services

public alert systems

## Zone-Based Mapping

All data is processed at a delivery zone level:

mapped using pin codes or geo-coordinates

linked to dark stores

ensures relevance for each worker

## Event Generation

When a trigger condition is satisfied:

A Disruption Event is created with:

event type (rain, pollution, etc.)

affected delivery zone

timestamp

severity level

source data reference

This event is then sent to the Claims Engine.

## Performance

data polling interval: ≤ 15 minutes

event detection latency: < 60 seconds

near real-time system response

## Reliability & Fallback

To ensure consistency:

multiple data sources used where possible

cached data used during API failures

automatic fallback mechanisms

error logging for monitoring

## Key Characteristics

Real-Time Detection
Immediate identification of disruptions

Objective Triggers
Based on measurable data

Automated Event Generation
No manual intervention

Scalable Design
Supports multiple cities and zones

## Why This Matters

The Trigger System is the foundation of GigShield.

Without accurate detection:

claims cannot be generated

payouts cannot be triggered

system reliability breaks

```text
By ensuring precise and real-time detection, GigShield enables:

fair compensation

fast response

scalable insurance operations
