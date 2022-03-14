---
layout: default
title: NMF
parent: Interfaces
---


## Nanosat MO Framework

[Link](https://github.com/esa/nanosat-mo-framework)


Relavent API specification in the NMF layer.




```java
// units is rads/sec

void setAllReactionWheelSpeeds(float wheelX, float wheelY, float wheelZ, float wheelU, float wheelV, float wheelW);
```


```java
// units are mAm^2 in the actuator frame

void setAllMagnetorquersDipoleMoments(float dipoleX, float dipoleY, float dipoleZ);
```