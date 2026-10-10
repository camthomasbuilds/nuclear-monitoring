# Case Study: Nuclear Equipment Health Monitoring Platform

## Context

Nuclear power plants operate under strict regulatory requirements where unplanned equipment failures are extremely costly, both in direct repair costs and in lost generation (a forced outage day can cost $3M+). Equipment health monitoring existed but was largely manual. Operators relied on periodic inspections, threshold alarms, and institutional knowledge to detect degradation.

## My Role

Senior Product Manager: responsible for defining the product vision, managing the delivery roadmap, and coordinating across nuclear engineering, IT, and third-party development teams.

## Problem Framing

**Operational challenges:**
- Health monitoring was manual or alarm-based. Degradation between inspection intervals went undetected
- Work order creation required manual data entry, creating duplicate efforts and backlog accumulation
- No systematic way to connect equipment condition data to maintenance scheduling decisions
- Scaling from a handful of monitored systems to plant-wide coverage required a platform, not point solutions

**Product opportunity:** Deliver a system that continuously monitors equipment health, detects anomalies early enough to schedule preventive maintenance, and reduces the manual overhead of work order management.

## Product Strategy

I structured the roadmap around progressive capability expansion:

1. **Foundation**: Integration with plant data historians, baseline physics models for initial equipment set
2. **Anomaly detection**: Layer data-driven anomaly detection on top of physics-based baselines to catch deviations that rule-based alarms miss
3. **Workflow automation**: Auto-generate work orders and condition reports from detected anomalies, reducing manual entry and backlog
4. **Fleet expansion**: Extend from pilot systems to 30+ monitored systems across multiple generating units

## Key Decisions

### Physics-based + data-driven hybrid
- **Decision:** Combine first-principles physics models with statistical anomaly detection rather than purely data-driven ML
- **Rationale:** Nuclear regulatory environments require explainability. A physics model provides a baseline that operators and regulators understand. Statistical methods catch subtle deviations the physics model doesn't predict. The combination provides both trust and sensitivity.

### In-house platform vs. vendor solution
- **Decision:** Build on a configurable platform with in-house customization rather than a pure off-the-shelf vendor product
- **Rationale:** Vendor solutions covered generic monitoring but didn't integrate with the plant's specific work management systems or regulatory workflows. A platform approach allowed custom integration while reducing third-party costs by 80%.

### Progressive rollout by system criticality
- **Decision:** Start with the highest-consequence systems (where a failure would cause the longest outage) rather than the easiest to instrument
- **Rationale:** This front-loaded the highest business value and proved the concept on the systems that mattered most to plant leadership.

## Results

- Reduced third-party costs by 80% ($1M O&M savings) through in-house platform development
- Decreased Work Order backlog by 10% via automation of previously manual entry processes
- Established architecture supporting expansion from 6 to 30+ monitored systems
- Enabled proactive condition-based maintenance, reducing forced outage risk
- Delivered Go/No-Go milestone for initial release

## Lessons Learned

1. **Regulatory trust is a product requirement**: In nuclear, a monitoring system that operators don't trust is worse than useless (they'll ignore it and rely on manual checks). Building trust required explainable models, gradual rollout, and early operator involvement in validation.

2. **Work order automation is higher-value than detection**: The monitoring itself was important, but the real time savings came from automating the downstream workflow (work order creation, scheduling integration). Detection without action is just more noise.

3. **Third-party cost reduction requires a platform bet**: The 80% cost reduction only materialized because we invested in a configurable platform rather than paying for bespoke vendor engagements per system. This was a deliberate product strategy, not just a cost-cutting exercise.
