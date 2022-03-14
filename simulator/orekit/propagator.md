---
layout: default
title: Propagator
parent: Orekit
grand_parent: Simulator
has_children: true
---

## Propagator

In Orekit Propagators give us a way to continue our orbit through time.


### Keplerian Propagator

The Keplerain Propagator with propagate the orbits with respect to keplers equations. In () the approach for using these systems was to use __attitude provider modifiers__ to analytically update the velocity and acceleration due to the reaction wheels and magnetorquers.

This approach has some issues however, as while working on this project I discovered an issue in their code which leads to incorrect acceleration values.

### Numerical Propagator

Numerical Propagator works by allowing us to add separate force models. For a system with distinct forces, this more cleanly separates the separate stages.