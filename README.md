---
editor_options: 
  markdown: 
    wrap: sentence
---

# Stat-950-Project

## Change-Point Detection in Logistic and Epidemic Models: Computational and Inferential Consequences

Change-point detection in nonlinear dynamical systems presents fundamental challenges for both statistical inference and computation.
This project investigates change-point detection in two nonlinear growth models: a logistic growth model and a Susceptible-Infected-Recovered (SIR) epidemic model.
For each model, we implement maximum likelihood estimation via profile likelihood search, parametric bootstrap, and Bayesian inference via Metropolis-within-Gibbs Markov chain Monte Carlo.
Simulation studies confirm that both models recover true parameters with negligible bias, and the change-point parameter is estimated with high accuracy under both inferential paradigms.

A key finding is that change-point identifiability differs fundamentally between the two models.
In the logistic model, the posterior for $\tau$ spreads across two adjacent values, while in the SIR model it collapses to a point mass at the true value, a consequence of the transmission rate change propagating through the entire coupled ODE(ordinary differential equation) system.
Bootstrap and Bayesian intervals show broadly consistent conclusions in both models, though differences in interval width reflect how each method captures uncertainty and parameter dependence, particularly in the SIR setting.
Computationally, the SIR model is substantially more expensive, requiring ODE solving at every likelihood evaluation and making estimation significantly slower than in the logistic case.
These results demonstrate that model mechanistic complexity has direct and quantifiable consequences for both inferential precision and computational cost.
