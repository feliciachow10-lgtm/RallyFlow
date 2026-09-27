# RallyFlow 🏐

### A rally-level volleyball analytics tool for studying first-ball side-out performance

RallyFlow is a volleyball data collection and analytics project designed to investigate what happens between serve receive and a team's first attack.

Traditional pass ratings summarize reception quality, but they do not fully capture where the pass goes, how far the setter must move, whether the offense stays in-system, what attacking options become available, or how these factors relate to first-ball side-out success.

RallyFlow was built to collect these spatial and contextual variables at the rally level and analyze how they interact.

## Research Question

**What factors are associated with successful first-ball side-outs in volleyball?**
## How RallyFlow Works

RallyFlow is a custom data-collection tool built to record the sequence of events from serve receive through the first attack.

For each rally, the tool can record information across four stages:

**Serve Receive**
- Pass rating (0–3)
- Pass contact and destination coordinates
- Reception technique

**Setter Movement**
- Setter starting position
- Ideal passing target
- Setter contact position
- Displacement from the ideal target
- Total setter travel

**Offensive Context**
- In-system vs. out-of-system
- Set location
- Rotation
- Number of blockers faced

**Attack**
- Attack type
- Attack contact and destination coordinates
- Attack outcome
- First-ball side-out success

This creates a rally-level dataset that connects traditional volleyball statistics with spatial and contextual information.
