# Earth–Sun Orbit: Forward Euler (v0.1)

**Status: Work in progress.** This notebook is an early portfolio project toward a validated N-body orbital mechanics simulator. It currently models one moving Earth under the gravity of a fixed Sun.

## What it does

The notebook uses Newtonian gravity and the forward Euler method to simulate an idealized 365-day Earth–Sun orbit with one-hour time steps. It calculates the gravitational acceleration, advances position and velocity, and plots the resulting trajectory.

With the Sun fixed at the origin, the acceleration is `a(r) = -G M_sun r / |r|^3`. The initial speed is set to the circular-orbit value `v = sqrt(G M_sun / r_0)`.

## Run it

1. Install Python 3 and Jupyter.
2. Install the packages listed in [requirements.txt](requirements.txt).
3. Open [earth_sun_euler_v0_1.ipynb](earth_sun_euler_v0_1.ipynb) in Jupyter and run all cells.

## Scope and limitations

This is a learning-stage numerical model, not a validated ephemeris or general N-body simulator. The Sun is fixed, only one orbiting body is modeled, and forward Euler is not symplectic: numerical error can accumulate and orbital energy is not conserved. Interpret the notebook's plot with those limitations in mind.

## Planned work

- Track and quantify energy and angular-momentum error.
- Compare step sizes and check convergence against Keplerian expectations.
- Implement a symplectic method such as velocity Verlet.
- Extend the force model to multiple interacting bodies.
- Add Monte Carlo propagation of initial-condition uncertainty.

**Author:** Andro J. Romero C.
