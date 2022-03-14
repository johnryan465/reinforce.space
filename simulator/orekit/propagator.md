---
layout: default
title: Propagator
parent: Orekit
has_children: true
---

## Propagator

In Orekit Propigators give us a way to continue our orbit through time.


### Keplerian Propigator

The Keplerain Propigator with propigate the orbits with respect to keplers equations. In () the approach for using these systems was to use __attitude provider modifiers__ to analytically update the velocity and acceleration due to the reaction wheels and magnetorquers.

### Numerical Propigator

Numerical Propigator works by allowing us to add serperate force models. For a system with distint forces, this more cleanly seperates the seperate stages.