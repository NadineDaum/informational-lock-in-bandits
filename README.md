# Biased Learning & Informational Lock-In 🔐
*A Bandit Model of Exposure Bias*

Why do false or incomplete beliefs persist in information-rich environments?  
Is mislearning always a consequence of cognitive bias—or can it arise even when individuals update beliefs rationally?

In modern information environments, individuals are surrounded by data, yet misperceptions remain widespread. A common explanation points to motivated reasoning, heuristics, or ideological bias. While these forces matter, empirical evidence also shows that people do update beliefs when exposed to new information.
This project explores a complementary explanation: **mislearning driven by biased sampling rather than biased inference**. Instead of modeling psychological deviations from rationality, the project treats learners as *normatively correct* and asks whether learning can still fail when exposure itself is systematically skewed—by algorithms, defaults, or friction.

---

## Approach

Learning is modeled as a **single-agent, two-armed Bernoulli bandit**:

- Each arm represents an information source with fixed but unknown accuracy.
- The agent updates beliefs correctly using standard learning rules.
- Exposure is distorted by an *exogenous bias* that affects which sources are observed, not how information is processed.

Three canonical bandit algorithms are used as **normative benchmarks**:
- ε-greedy  
- UCB1  
- Thompson Sampling  

The goal is not to model human cognition, but to **stress-test rational learning** under biased exposure.

---

## Contents

- `informational-lock-in-bandits.ipynb`  
  Python notebook implementing the simulation and generating figures.

- `paper.pdf`  
  Final project paper (course: Algorithmic Game Theory, Fall 25).

- `figures/`  
  Output figures used in the paper.

---

## Reproducibility

All results can be reproduced by running `informational-lock-in-bandits.ipynb`.  
Random seeds are fixed at the run level and varied across independent repetitions.  
The code is written for clarity rather than performance and is fully self-contained.
This project was completed as part of an Algorithmic Game Theory course at Hertie.

---

*Questions, comments, or suggestions are welcome.*
