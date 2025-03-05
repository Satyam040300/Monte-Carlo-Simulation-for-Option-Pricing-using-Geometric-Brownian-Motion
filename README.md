# Monte Carlo Simulation for Option Pricing using Geometric Brownian Motion

This project implements a **Monte Carlo simulation** to price **European Call** and **Put** options using the **Geometric Brownian Motion (GBM)** model. It simulates multiple asset price paths and calculates the payoff at maturity, which is then discounted to the present value. This approach provides an approximation of the option price by averaging the discounted payoffs across all simulations.

## Project Overview

The project models the behavior of asset prices using the **Geometric Brownian Motion** process and applies **Monte Carlo methods** to estimate the price of both **Call** and **Put** options. The model simulates multiple paths for the asset price over time, and for each path, the corresponding payoff is computed at the option's maturity. The average of these payoffs, discounted to the present, gives an estimate of the option's price.

### Key Features:
- **Monte Carlo Simulation:** Simulates multiple asset price paths to estimate option prices.
- **Geometric Brownian Motion (GBM):** Used to model asset prices and simulate future movements.
- **Option Pricing:** Computes the price of European **Call** and **Put** options using Monte Carlo methods.

## How the Model Works

1. **Simulate Asset Price Paths:**
   The asset price is simulated using the following Geometric Brownian Motion formula:
   \[
   S(t+1) = S(t) \times \exp \left( \left( r - \frac{1}{2} \sigma^2 \right) \Delta t + \sigma \sqrt{\Delta t} Z \right)
   \]
   where \(S(t)\) is the asset price at time \(t\), \(r\) is the risk-free rate, \(\sigma\) is the volatility, \(\Delta t\) is the time step, and \(Z\) is a random variable from a standard normal distribution.

2. **Payoff Calculation:**
   For each simulated path, the **Call** and **Put** option payoffs are calculated:
   - **Call Option Payoff:** \( \max(S(T) - K, 0) \)
   - **Put Option Payoff:** \( \max(K - S(T), 0) \)
   where \(S(T)\) is the simulated asset price at maturity, and \(K\) is the strike price.

3. **Discount the Payoff:**
   The payoff for each path is discounted to the present value using the risk-free rate:
   \[
   \text{Option Price} = \exp(-r \times T) \times \text{mean(Payoffs)}
   \]

## Project Structure

- `Satyam_Monte_Carlo_Call_Option_Pricing_Using_Geometric_Brownian_Motion_(GBM).ipynb`: Contains the main functions to simulate asset price paths, calculate the option payoffs, and estimate the prices of the **Call** and **Put** options.
- `README.md`: This file, providing an overview of the project.

## Skills Learned

- **Monte Carlo Simulation**: Gained practical experience in applying Monte Carlo methods to price financial options.
- **Geometric Brownian Motion (GBM)**: Applied GBM to model stock price movements.
- **Numerical Methods in Finance**: Used numerical simulations to approximate the price of financial derivatives.
- **Python Programming**: Enhanced Python skills, particularly with **NumPy** for generating random numbers and performing matrix operations.

## Requirements

- Python 3.x
- NumPy (for numerical calculations and random number generation)


