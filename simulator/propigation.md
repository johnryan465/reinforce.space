---
layout: default
title: Propagator
parent: Simulator
nav_order: 2
---


## Propigation


A _propigation_ is our prediction for how the state (including the attitude) will evolve with respect to time.

The simplest way to implement this is by using a FixedStepHandler. This is a function which given the previous state and a fixed time step, will generate the next state.

Orekit can then interpolate between the states which we have generated at our fixed time steps.

If we make our fixed time step sufficently stop, we can linearise the physics equations which we use to update the state.