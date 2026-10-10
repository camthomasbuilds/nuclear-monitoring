# Nuclear Equipment Health Monitoring

## The Business Problem

Nuclear power plants face $3M+/day forced outage costs. Equipment health monitoring was manual: operators relied on periodic inspections, threshold alarms, and institutional knowledge. Degradation between inspection intervals went undetected. Work order creation was manual, creating backlogs and duplicate effort. The organization needed to scale from monitoring a handful of systems to plant-wide coverage.

**The strategic question:** How do you build trust in AI in a regulated, zero-failure-tolerance environment?

## My Role

Senior Product Manager. Owned product vision, delivery roadmap, and coordination across nuclear engineering, IT, and third-party development teams.

## The Key Decisions

### 1. Physics + statistical hybrid (not black-box ML)

Nuclear regulatory environments require explainability. I chose a hybrid approach: first-principles physics models provide baselines that operators and regulators understand; statistical methods catch subtle deviations the physics models miss. The combination provides both trust and sensitivity. A pure ML approach would have been rejected on day one.

### 2. In-house platform over vendor solution

Vendor solutions covered generic monitoring but couldn't integrate with the plant's specific work management systems or regulatory workflows. I made the platform bet: invest in a configurable in-house platform that enables custom integration. Result: 80% cost reduction ($1M O&M savings) compared to bespoke vendor engagements per system.

### 3. Start with highest-consequence systems

Conventional wisdom says pilot on the easiest systems first. I chose the highest-consequence systems (where failure causes the longest outages). This front-loaded business value and proved the concept on the systems that mattered most to plant leadership. If it works on the hardest case, everything else is easier to fund.

### 4. Phased trust-building

I structured the rollout in four phases: display data accurately (prove you can read), surface anomalies (prove you can detect), recommend actions (prove you can think), automate low-risk decisions (prove you can act). Each phase had explicit success criteria before advancing. This earned operator trust incrementally rather than demanding it upfront.

## Results

| Metric | Outcome |
|--------|---------|
| **Cost reduction** | 80% reduction in third-party monitoring costs ($1M O&M savings) |
| **Backlog** | 10% decrease in work order backlog through automation |
| **Scale** | Architecture supports expansion from 6 to 30+ monitored systems |
| **Outage prevention** | Proactive condition-based maintenance reducing forced outage risk |
| **Governance** | Go/No-Go milestone delivered for initial production release |

## What This Demonstrates

- **Trust engineering** in regulated environments (phased rollout with explicit gates)
- **Build vs. buy judgment** (platform bet that delivered 80% cost reduction)
- **Stakeholder management** in safety-critical domains (operator trust as a product requirement)
- **Vendor-to-platform migration** (replacing point solutions with scalable architecture)
