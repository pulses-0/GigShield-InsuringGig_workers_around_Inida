# 10. Insurance Coverage Model

The Insurance Coverage Model defines how GigShield calculates compensation for delivery partners when a valid disruption event occurs.

The model is designed to provide partial income protection that is predictable, proportional, and financially sustainable.

---

## 10.1 Objectives

The primary objectives of the coverage model are:

- compensate for loss of earning opportunity during disruptions  
- provide timely financial support aligned with gig worker cash flow  
- maintain fairness and consistency across users  
- ensure long-term sustainability of the system  

The model does not aim to fully replace income, but to reduce the financial impact of disruptions.

---

## 10.2 Coverage Structure

GigShield offers three levels of coverage:

| Coverage Tier | Protection Level |
|--------------|----------------|
| Basic        | Up to 40% of income loss |
| Standard     | Up to 60% of income loss |
| Premium      | Up to 80% of income loss |

The selected coverage tier directly determines the payout percentage.

---

## 10.3 Income Estimation

The system estimates user income using:

- average weekly delivery count  
- per-delivery earnings  
- recent activity trends  

From this, an estimated hourly income is derived:

```text
Estimated Hourly Income =
Estimated Weekly Income / Total Active Hours
10.4 Payout Calculation

Payouts are calculated using the following formula:

Payout =
Estimated Hourly Income × Disruption Duration × Coverage Percentage

Where:

Disruption Duration is measured in hours

Coverage Percentage depends on the selected plan

10.5 Example

A delivery partner:

earns ₹200 per hour

experiences disruption for 2 hours

has selected Standard coverage (60%)

Calculation:

Payout = 200 × 2 × 0.6 = ₹240
10.6 Trigger Duration Requirement

To ensure meaningful payouts:

a minimum disruption duration is required (e.g., ≥ 1 hour)

short-lived spikes do not trigger payouts

This prevents unnecessary micro-payouts.

10.7 Weekly Claim Limits

To maintain system sustainability:

the number of payable events per week is capped

example: maximum 2–3 claims per coverage period

This avoids excessive claims and misuse.

10.8 Maximum Payout Cap

A cap is applied to total weekly payouts:

payout cannot exceed a percentage of weekly income

ensures financial stability of the system

10.9 Multi-Event Handling

If multiple disruption events occur in overlapping time windows:

overlapping durations are merged

payouts are calculated on unique time intervals

Example:

IF events overlap
THEN merge durations
10.10 Payout Timing

payout initiation: within 2 minutes of approval

payout completion: near real-time (mock system)

10.11 Edge Case Handling

The system accounts for:

partial-hour disruptions (rounded using defined rules)

sudden fluctuations (filtered using duration thresholds)

conflicting data (validated before payout)

10.12 Design Considerations

The model is designed to be:

transparent and explainable

fair across different user types

resistant to abuse

scalable across large user bases

10.13 Importance

The coverage model directly determines:

user trust in the system

fairness of payouts

financial sustainability

A well-balanced model ensures that GigShield remains both useful to workers and viable as a platform.
