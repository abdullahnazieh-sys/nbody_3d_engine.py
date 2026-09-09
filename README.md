# 3D $N$-Body Gravitational & Chaos Simulator

A computational physics engine built in Python that models multi-body gravitational systems in 3D space. It validates numerical stability using **4th-Order Runge-Kutta (RK4)** integration and quantifies chaotic sensitivity (the Butterfly Effect) in real time.

![Simulation Demo](assets/demo.gif)

## Key Computational & Physics Features

* **4th-Order Runge-Kutta (RK4) Integration:** Solves non-linear coupled differential equations in 3D to accurately track position ($\mathbf{r}$) and velocity ($\mathbf{v}$) without artificial numerical decay.
* **Gravitational Softening ($\epsilon$):** Incorporates a softening parameter in Newton's Law of Universal Gravitation ($\mathbf{F} = G \frac{m_1 m_2}{r^2 + \epsilon^2}$) to prevent numerical singularities during close encounters.
* **Chaotic Sensitivity & Lyapunov Divergence:** Runs two identical 3-body systems in parallel with a initial perturbation of $\delta z = 10^{-5}$ on a single body to track exponential divergence on a live log-scale plot.
* **Analytical Solutions (Figure-8 Orbit):** Includes initial conditions for the stable 3-body periodic Figure-8 solution (discovered by Chenciner & Montgomery).
* **3D Matplotlib Rendering:** Live 3D trajectory tracking with orbiting camera perspective and dynamic path trailing.

## Tech Stack
* **Language:** Python 3
* **Libraries:** NumPy (Vectorized Math), Matplotlib (3D Animation & Plotting)

## How to Run

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/nbody-gravitational-simulator.git](https://github.com/your-username/nbody-gravitational-simulator.git)
   cd nbody-gravitational-simulator# nbody_3d_engine.py
