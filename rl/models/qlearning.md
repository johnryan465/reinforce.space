---
layout: default
title: Q Learning
parent: RL Models
grand_parent: Reinforcement Learning
math: mathjax3
---

## Q Learning

### The Bellman Equation

The [Bellman equation](https://en.wikipedia.org/wiki/Bellman_equation) is a necessary condition for an optimum solution for a dynamic programming problem.


$$V(x) = \max_{a \in \Gamma (x)} F(x, a) + \beta V(T(x,a)) $$

Where $T(x,a)$ represents the new state, $F(x,a)$ is the immediate reward.$V(x)$

---

We can view RL as a dynamic programming problem, and converting it to the language of MDPs we get the following corresponding equation.

With an optimum policy, it will obey the __Bellman Optimality Equation__.

$$q^\prime(s, a) = E\left[R_{t+1} + \gamma \max_{a^\prime} q^\prime (s^\prime, a^\prime) \right] $$

In Q-Learning we iteratively improve our policy by using __value iteration__.

