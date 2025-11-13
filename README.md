# Agent-Based Modeling of Pandemic Spread

**Author:** Ken Su  
**Email:** ken.su@emory.edu  
**In response to:** Question 2 - Agent-Based Modeling of Pandemic Spread

---

## Overview

This repository contains responses to Question 2 from Model_Based_Machine_Learning_HW. In the ipynb notebook, I conducted experiments on agent-based pandemic spread simulation under different scenarios.

---

## Experimental Setup

### Initial Configuration

In the problem statement, the default parameters for grid size is 75 * 75, populated with 100 agents of which 5 are infected (I), 95 are susceptible (S), and 0 are recovered (R). 

### Configuration Issues and Adjustments

Under this set-up I conducted initial experiment for Part A, while realizing that the grid size is too large for 100 agents to run an effective simulation of pandemic, since it would be a rare event for agents to come into contact. Under that setup, the peak infection always happens at the beginning (time step 0) since it doesn't spread out. 

Therefore, for the following experiments on social distancing measures, I used **10 * 10 grid** and **100 agents** of which **30 are infected (I)**, **70 are susceptible (S)**, and **0 are recovered (R)** for a more effective and realistic simulation of pandemic spread.

---

## Key Insights Regarding Social Distancing

### Peak Infection and Time to Peak

In terms of the peak number of infected individuals and time to peak, without social distancing measures, with 10 simulations under random initial conditions:

- **Baseline model (without social distancing, p_infection=0.9):** Average of **70.9 individuals** at peak infection, reaching the peak in **6 time steps**

- **With social distancing measures (p_infection=0.3):** Average of **51.3 individuals** at peak infection, reaching the peak in **12 time steps**

### Interpretation

This indicates that social distancing measures effectively reduce the peak number of infections and delay the time to peak, which can help alleviate pressure on healthcare systems during a pandemic. This is also reflected by a flatter number of infected curve.

However, the time steps taken to reach a neutralized state (where infections drop to zero and no new infections occur) appears to be longer with social distancing, as the disease both spreads and ends more slowly through the population.

### Real-World Implications

In real-world scenarios, implementing social distancing could be a crucial strategy to manage healthcare resources and reduce the overall impact of a pandemic, since medical resources are often limited, and more effective treatment measures could come out over time, such as vaccines and antiviral drugs. 

The trade-off would be a longer time span of the pandemic, but should be a secondary consideration comparing to overwhelming the healthcare system at peak infection times.

---

## Model Comparison

### Experimental Design

Experiments with different p_infection values to simulate varying strengths of social distancing measures, each for 10 runs with random initial conditions and taken the average.

### Results

The baseline experiment was conducted at **p_infection=0.9**, which reflects the scenario without social distancing. Then for the subsequent experiments:

- **Experiment 1:** p_infection=0.3, simulating moderate social distancing → Peak infected: **51.3**, Time to peak: **12**

- **Experiment 2:** p_infection=0.15, simulating strong social distancing → Peak infected: **36.0**, Time to peak: **13**

- **Experiment 3:** p_infection=0.6, simulating weak social distancing → Peak infected: **68.1**, Time to peak: **6**

### Conclusion

This corresponds with the expectation that stronger social distancing (lower p_infection) leads to a lower peak number of infections and a delayed time to peak, effectively flattening the infection curve.

---

## Disclaimer

VSCode CoPilot Auto-complete was used to complete HW #2.A and #2.B to auto-complete unfinished Python code sentence/variable names. Since auto-completion is passive Generative AI, it doesn't involve any prompt or response.

---

