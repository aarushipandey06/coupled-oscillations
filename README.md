# Coupled Oscillations: Numerical Simulation and Analysis

## Overview

This project investigates the motion of two identical masses connected by three identical springs. The equations of motion are solved numerically to study the system's oscillatory behaviour, energy conservation, and normal-mode frequencies.

The numerical results are compared with theoretical predictions to examine the accuracy and limitations of the integration methods.

## Physical Model

The system consists of two masses, each of mass $m$, connected by three springs, each with spring constant $k$. The outer springs are attached to fixed walls, and the middle spring couples the two masses.

The equations of motion are

$$
\ddot{x}_1 = \frac{-2kx_1+kx_2}{m}
$$

$$
\ddot{x}_2 = \frac{kx_1-2kx_2}{m}
$$

The theoretical normal-mode frequencies are

$$
f_1 = \frac{1}{2\pi}\sqrt{\frac{k}{m}},
\qquad
f_2 = \frac{1}{2\pi}\sqrt{\frac{3k}{m}}.
$$

For the parameters used in this simulation, $m=1.0\,\mathrm{kg}$ and $k=1.0\,\mathrm{N/m}$, the theoretical frequencies are approximately $0.15915\,\mathrm{Hz}$ and $0.27566\,\mathrm{Hz}$.

## Methods

- **Euler integration:** Numerical solution of the equations of motion.
- **Energy analysis:** Calculation of kinetic, potential, and total mechanical energy.
- **Timestep convergence:** Comparison of energy errors for different timestep sizes.
- **Euler vs RK4:** Comparison of energy stability over a longer simulation.
- **FFT analysis:** Estimation of the normal-mode frequencies from simulated displacement data.

## Key Results

- The Euler method exhibits increasing energy drift over time.
- Reducing the timestep decreases the final energy error in the Euler simulation.
- RK4 maintains much better energy stability than Euler for the tested parameters and simulation duration.
- The FFT estimates are close to the theoretical normal-mode frequencies, with discrepancies influenced by finite frequency resolution.

## Tools and Libraries

- Python
- NumPy
- Matplotlib
- SciPy

## How to Run

Open `coupled_oscillations.ipynb` in Google Colab or Jupyter Notebook.

Install the required libraries using:

```bash
pip install -r requirements.txt
```

Run the notebook cells in order to reproduce the simulations, plots, energy analysis, and frequency calculations.

## Scope

This project explores numerical integration and error analysis for a coupled mechanical system. It illustrates how numerical methods can be used to compare simulated behaviour with analytical predictions.
