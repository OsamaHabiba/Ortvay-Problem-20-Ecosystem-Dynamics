# Ortvay-Problem-20-Ecosystem-Dynamics
# Analysis of a Three-Species Ecosystem under Radioactive Effects

This repository contains the numerical solution and theoretical derivation for **Problem 20** of the **Rudolf Ortvay International Problem Solving Contest in Physics**. The project investigates the stability and equilibrium of a three-level trophic ecosystem subjected to a constant radiation-induced mortality rate.

## Problem Statement

An isolated ecosystem consists of three trophic levels:
1.  **Plants ($N_1$)**: Productive level.
2.  **Herbivores ($N_2$)**: Primary consumers.
3.  **Carnivores ($N_3$)**: Secondary consumers.

The populations are modeled as a continuous deterministic system. The introduction of radioactive material adds a uniform death rate $q$ to all species:

$$\frac{dN_i}{dt} = N_i f_i(N_1, N_2, N_3) - qN_i$$

The goal is to determine how the stable equilibrium changes with $q$ and identify the critical threshold $q_c$ at which the ecosystem stability ceases.

## Mathematical Model

The dynamics are governed by a modified Lotka-Volterra system for three species:

$$\begin{aligned}
\frac{dN_1}{dt} &= rN_1 \left(1 - \frac{N_1}{K}\right) - aN_1N_2 - qN_1 \\
\frac{dN_2}{dt} &= eaN_1N_2 - bN_2N_3 - m_2N_2 - qN_2 \\
\frac{dN_3}{dt} &= cbN_2N_3 - m_3N_3 - qN_3
\end{aligned}$$

Where:
- $r$ is the plant growth rate and $K$ is the carrying capacity.
- $a, b$ are predation rates.
- $e, c$ are efficiency constants.
- $m_i$ are natural mortality rates.
- $q$ is the radiation-induced death rate.

## Key Findings

- **Equilibrium Shift**: As $q$ increases, the equilibrium populations of the higher trophic levels (carnivores) decline more rapidly than the producers.
- **Critical Threshold**: There exists a critical value $q_c \approx 0.214$ (based on the provided parameters) where the carnivore population collapses.
- **System Breakdown**: Beyond $q_c$, the three-species chain breaks down into a simpler two-species or one-species system.


