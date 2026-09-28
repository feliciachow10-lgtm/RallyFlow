# RallyFlow Dataset

## Overview

The RallyFlow pilot dataset contains **121 annotated volleyball rallies** collected from match film.

Each row represents one rally and connects serve-receive, setter movement, offensive context, attack information, and rally outcome.

The pilot dataset was created primarily to test RallyFlow's data-collection system and explore which variables may be useful for future volleyball analysis.

## Main Variable Groups

### Serve Receive

Variables include:

- Traditional pass rating (0–3)
- Pass contact coordinates
- Setter contact / pass destination coordinates
- Reception technique
- Serve information

### Setter Movement

Variables include:

- Setter starting coordinates
- Ideal passing target
- Setter contact coordinates
- Setter displacement from the ideal target
- Total setter travel

### Offensive Context

Variables include:

- Rotation
- In-system vs. out-of-system status
- Set location
- Number of blockers faced

### Attack

Variables include:

- Attack type
- Attack contact coordinates
- Attack destination coordinates
- Attack outcome

### Outcomes

The primary outcome used in the pilot analysis is:

**First-ball side-out success**

A successful first-ball side-out occurs when the receiving team wins the rally with its first attack following serve receive.

## Sample Sizes

Although the complete pilot contains 121 rallies, not every variable applies to every rally.

For example, a rally may end before a normal attack occurs, or a particular spatial measurement may not be available. Because of this, the sample size varies between analyses.

The analysis notebook reports the relevant sample sizes for each question.

## Data Availability

The raw pilot dataset is not currently included in the public repository.

Before publishing rally-level data, I want to make sure that any identifying information related to players, teams, matches, or source video is handled appropriately.

An anonymized version of the dataset may be added as RallyFlow develops.
