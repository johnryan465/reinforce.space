---
layout: default
title: Force Models
parent: Custom Simulator
grand_parent: Simulator
nav_order: 2
---

# Force Model




---

Example: Maneuver from Orekit

```java
@Override
public <T extends CalculusFieldElement<T>> void addContribution(final FieldSpacecraftState<T> s,
                    final FieldTimeDerivativesEquations<T> adder) {

    final T[] parameters = getParameters(s.getDate().getField());
    if (maneuverTriggers.isFiring(s.getDate(), getManeuverTriggersParameters(parameters))) {
        // Compute thrust acceleration in inertial frame
        adder.addNonKeplerianAcceleration(acceleration(s, parameters));

        // Compute flow rate using the propulsion model
        // Specific drivers for the propulsion model are extracted from the array given by the ForceModel interface
        adder.addMassDerivative(propulsionModel.getMassDerivatives(s, getPropulsionModelParameters(parameters)));
    }
}
```

```java
@Override
public Vector3D acceleration(final SpacecraftState s, final double[] parameters) {

    // If the maneuver is active, compute and add its contribution
    // Maneuver triggers are used to check if the maneuver is currently firing or not
    // Specific drivers for the triggers are extracted from the array given by the ForceModel interface
    if (maneuverTriggers.isFiring(s.getDate(), getManeuverTriggersParameters(parameters))) {

        // Attitude during maneuver
        final Attitude maneuverAttitude =
                        attitudeOverride == null ?
                        s.getAttitude() :
                        attitudeOverride.getAttitude(s.getOrbit(),
                                                        s.getDate(),
                                                        s.getFrame());

        // Compute acceleration from propulsion model
        // Specific drivers for the propulsion model are extracted from the array given by the ForceModel interface
        return propulsionModel.getAcceleration(s, maneuverAttitude, getPropulsionModelParameters(parameters));
    } else {
        // Constant (and null) acceleration when not firing
        return Vector3D.ZERO;
    }
}
```


---
## Magnetorquers Force Model




```java
void addContribution(SpacecraftState s, TimeDerivativesEquations adder)
```

## Reaction Wheel Force Model

