# Option Pricing using a Control Variate (Monte Carlo Simulation)

The content of this notebook is based on Chapter 4 of the book "Monte Carlo Methods in Financial Engineering" by Paul Glasserman. <br>

## Overview

This project implements a Monte Carlo simulation for pricing a European call option under the Geometric Brownian Motion (GBM) model.

To improve the efficiency and accuracy of standard Monte Carlo estimation, the project applies **control variates method** as a variance reduction technique.

The goal is to compare the performance (variance and convergence speed) between a standard Monte Carlo estimator and a control variate estimator.

---

## Model Assumption

The underlying stock price follows a Geometric Brownian Motion (GBM):

$$\frac{dS(t)}{S(t)} = r dt + \sigma dW(t)$$

where:
- $S(t)$: stock price at time t  
- $r$: risk-free interest rate  
- $\sigma$: volatility  
- $W(t)$: Wiener process

---

## Option Type

- European Call Option
- Payoff: max(S(T) - K, 0)

---

## Method

### Standard Monte Carlo
- Simulate the path of stock prices $S(t)$ using GBM
- Compute discounted payoff
- Compute call option values
- Take average over all paths

### Control Variates
- Simulate the path of stock prices $S(t)$ using GBM
- Compute discounted payoff
- Compute call option values
- Use terminal stock price $S(t)$ as a control variate
- Take average over all paths

---

## Features

- GBM-based stock price simulation
- European call option pricing
- Standard Monte Carlo estimator
- Control variates method implementation
- Confidence interval comparison between methods

---

## Tech Stack

- Python
- NumPy

---

## Results

Sampling with a control variate shows:
- Lower variance (i.e., narrower confidence interval) compared to standard Monte Carlo

---

## References

1. Glasserman, P. (2003) *Monte Carlo Methods in Financial Engineering*. Springer, New York.

---
