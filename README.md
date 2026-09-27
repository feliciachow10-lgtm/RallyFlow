# RallyFlow 🏐

### Looking beyond the 0–3 pass rating to understand what actually creates a successful first-ball side-out

I started RallyFlow because, as a volleyball player, I kept wondering how much a traditional 0–3 pass rating actually tells us. Two passes can get the same rating but put the setter in completely different positions, change which hitters are available, and lead to very different attacks.

That made me curious about what we might be missing when we reduce an entire serve-receive play to one number. I built RallyFlow to track what happens throughout the play—from where the pass goes and how far the setter moves to where the attack lands—and then analyze how those factors relate to first-ball side-out success.

## Research Question

**What factors are associated with successful first-ball side-outs in volleyball?**

## How RallyFlow Works

I use RallyFlow while watching match film to record what happens from the serve through the first attack. Instead of only recording the outcome of the play, I wanted to capture what actually happened on the court leading up to it.

<p align="center">
  <img src="ChatGPT Image Sep 26, 2026, 09_46_43 PM.png" alt="RallyFlow data collection interface" width="900">
</p>

*RallyFlow's annotation interface combines video review with interactive court coordinates and rally-level data collection.*

For each rally, I can record:

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

Putting all of this together creates a rally-level dataset where I can look at not only whether a team sided out, but also what happened throughout the play that may have contributed to that result.

## Pilot Study

I recently finished collecting my first **121 rallies**. Since this is still a pretty small dataset, I am treating this as a pilot study rather than trying to make broad conclusions about volleyball from it.

My main goal with this first analysis was actually to test RallyFlow itself: **Am I collecting data that can reveal useful patterns?** I also wanted to see which questions seem worth investigating further and where my data-collection process could improve before I build a much larger dataset.

Because some measurements do not apply to every rally or were missing in the original data, the sample size is different for each analysis.

### What I Wanted to Investigate

1. Does pass quality relate to first-ball side-out success?
2. What happens to first-ball side-out success as the setter moves farther from the ideal passing target?
3. How much does being in-system vs. out-of-system matter?
4. Does set location relate to first-ball side-out success?
5. Where are attacks landing, and does attack destination relate to effectiveness?
6. How does the number of blockers faced relate to first-ball side-out success?
7. Does first-ball side-out success differ by rotation?
8. When passes miss the ideal target, where are they actually going?
9. How much does the setter have to travel in each rotation?
## Methods

After collecting the 121 rallies, I cleaned the dataset and analyzed it using **Python, Google Colab, and Tableau**.

I definitely did not use the exact same statistical test for every question. The variables are different, so I tried to choose a method that actually made sense for each relationship I was looking at.

### How I Analyzed the Data

- **Logistic regression** — I used this when I wanted to see how a numerical variable, like pass rating or setter displacement, related to the probability of a successful first-ball side-out.

- **Fisher's exact test** — I used this for categorical comparisons with small sample sizes, including in-system vs. out-of-system rallies.

- **Permutation testing** — I used this when some groups had very few observations and the assumptions behind a traditional test were questionable.

- **ANOVA** — I used this to compare average setter travel across the six rotations.

- **Descriptive analysis** — For several of the more exploratory questions, I compared percentages, counts, averages, and spatial patterns without trying to make a strong statistical conclusion from such a small dataset.

### Visualizing the Data

I used **Tableau** for several of the comparison charts and **Python/Matplotlib** for the spatial court maps and some of the more customized visualizations.

One thing I learned pretty quickly was that a graph can look dramatic even when there are barely any observations behind it 🤦‍♀️. Because of that, I included sample sizes in my visualizations and tried to be careful about separating an interesting pattern from something I could actually support statistically.
## Key Findings

### 1. Better passes were strongly connected to first-ball side-out success

This was probably the clearest pattern I found in the pilot data. As pass rating increased, first-ball side-out success increased with it.

- **0-pass:** 0.0% (0/16)
- **1-pass:** 3.7% (1/27)
- **2-pass:** 15.6% (7/45)
- **3-pass:** 47.6% (10/21)

<p align="center">
  <img src="First-Ball Side-Out Success by Pass Rating.png" alt="First-ball side-out success by pass rating" width="700">
</p>

A logistic regression also found a statistically significant positive relationship between pass rating and first-ball side-out success (**β = 1.284, p = .014**).

I expected better passes to lead to more successful side-outs, so that part was not exactly shocking 😭. What surprised me more was how large the difference was. A 3-pass resulted in a first-ball side-out almost half the time in this dataset, compared with only 15.6% for a 2-pass.

At the same time, I don't want to treat these percentages as universal volleyball benchmarks. This is still a small pilot dataset, and one of my next goals is to see whether the same pattern holds as I collect more rallies.
