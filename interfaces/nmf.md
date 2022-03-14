---
layout: default
title: NMF Setting
parent: Interfaces
---


## Nanosat MO Framework



Relavent API specification in the NMF layer.




```java
// units is rads/sec

void setAllReactionWheelSpeeds(float wheelX, float wheelY, float wheelZ, float wheelU, float wheelV, float wheelW);
```


```java
// units are mAm^2 in the actuator frame

void setAllMagnetorquersDipoleMoments(float dipoleX, float dipoleY, float dipoleZ);
```