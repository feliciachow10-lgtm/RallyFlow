# RallyFlow Pilot Analysis

## Overview

This page contains the full analysis from my first **121 rallies collected with RallyFlow**.

The main purpose of this pilot was not to make broad conclusions about volleyball performance. I wanted to test whether the variables I chose to collect could actually reveal useful patterns, figure out which measurements seemed worth keeping, and identify questions I want to investigate with a much larger dataset.

Because not every variable was available or applicable for every rally, **sample sizes vary between analyses**.

## Analysis Questions

1. [Pass Rating and First-Ball Side-Out](#1-pass-rating-and-first-ball-side-out)
2. [Setter Displacement and First-Ball Side-Out](#2-setter-displacement-and-first-ball-side-out)
3. [In-System vs. Out-of-System](#3-in-system-vs-out-of-system)
4. [Set Location](#4-set-location)
5. [Attack Destination](#5-attack-destination)
6. [Blockers Faced](#6-blockers-faced)
7. [Rotation](#7-rotation)
8. [Pass Destination and Miss Direction](#8-pass-destination-and-miss-direction)
9. [Setter Travel by Rotation](#9-setter-travel-by-rotation)

---

## 1. Pass Rating and First-Ball Side-Out

### Question

**Does traditional pass rating (0–3) relate to first-ball side-out success?**

### Results

First-ball side-out success increased as pass rating improved:

| Pass Rating | Successful Side-Outs | Total | Success Rate |
|---|---:|---:|---:|
| 0 | 0 | 16 | 0.0% |
| 1 | 1 | 27 | 3.7% |
| 2 | 7 | 45 | 15.6% |
| 3 | 10 | 21 | 47.6% |

Logistic regression found a statistically significant positive relationship between pass rating and first-ball side-out success (**β = 1.284, p = .014**).

<p align="center">
  <img src="../01_pass_rating.png" alt="First-ball side-out success by pass rating" width="700">
</p>

### What I Took From This

This was probably the least surprising result of the pilot—better passes leading to better offensive outcomes makes sense. But that was actually useful. One of my first questions was whether RallyFlow was collecting data that could reproduce relationships I would expect to see in actual volleyball.

The more interesting question for me became whether RallyFlow's spatial measurements could tell me anything **beyond** the traditional pass rating.

---
