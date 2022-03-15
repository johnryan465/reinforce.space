---
layout: default
title: Force Models
parent: Custom Simulator
grand_parent: Simulator
nav_order: 2
---

# Force Model




---

Example: Simplified Maneuver from Orekit

```java
public <T extends CalculusFieldElement<T>> void addContribution(final FieldSpacecraftState<T> s,
                    final FieldTimeDerivativesEquations<T> adder) {
    final T[] parameters = getParameters(s.getDate().getField());
    // Compute thrust acceleration in inertial frame
    adder.addNonKeplerianAcceleration(acceleration(s, parameters));
    // Compute flow rate using the propulsion model
    // Specific drivers for the propulsion model are extracted
    // from the array given by the ForceModel interface
    adder.addMassDerivative(propulsionModel.getMassDerivatives(s, getPropulsionModelParameters(parameters)));
}
```

We will need to 

---
## Magnetorquers Force Model




```java
void addContribution(SpacecraftState s, TimeDerivativesEquations adder)
```

## Reaction Wheel Force Model

