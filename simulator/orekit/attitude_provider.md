---
layout: default
title: Attitude Provider
parent: Orekit
grand_parent: Simulator
nav_order: 2
---


## Attitude Provider

An __attitude provider__ is a class which will return the attitude and position-velociry state at a particular time with respect to a particular refernce frame.

### Kinematics

The __Kinematics__ provider takes the previvous attitude, and updates the attitude by linearisng the rotation update equation. The rotation is with respect to the centre of the Earth (done in the Earth Centred Inertial Frame)

The linearisation equation can be understood from [here](https://fgiesen.wordpress.com/2012/08/24/quaternion-differentiation/)

### Kinetics

The __Kinetcs__ provider updates the spin in the satillite fram and the angular accelleration.

This step is where we take in the forces  which are acting on the satillite and use these to update the required values.
