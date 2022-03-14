---
layout: default
title: Custom Simulator
parent: Simulator
has_children: true
---


## Custom Simulator

For this project we have written a custom simulator for our RL Loop.

- Usable in Python (with Pytorch)
- Compatibility with the NMF simulator
- Ability to implement reaction wheels and magnetorquers.



The solution used in this project is to use the Orekit Python bindings.


---

## Design

- Use Orekit Python Bindings
- Use the Numerical Propagator
- Add force model for reaction wheel and magnetorquers.
- Add a function for the controller to update their state.
