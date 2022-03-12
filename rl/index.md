---
layout: default
title: Reinforcement Learning
nav_order: 2
has_children: true
---


# Reinforcement Learning

## Markov Decision Process

A markov descision process is a tuple $(S,A,P,R)$ where

- $S$ is a set or states
- $A$ is a set of actions (which might be dependent on the current state)
- $P$ is a family of functions which define the probability of state transitions given a specific action.
- $R$ describes the reward recieved after when going from $s$ to $s\prime$ given action $a$.


For a particular Markov Desicion Process our objective in RL is to synthesis a __policy__, which describes what we will do in a particular state to maximise some objective.

A common approach is to attempt to maximise the expected discounted reward. This is often necessary as simpky taking the expected reward might lead to some policies having an infinite reward.


## Model Free vs Model Based

In Model Free RL we do not attempt to explicitly model the transition functions and reward functions, we simply use the data which we aquire.

In Model Based RK we 