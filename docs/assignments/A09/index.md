# A9 – Pulleys

## Objective:

The objective of this project is to design a pulley and belt system capable of transferring rotational power between two parallel shafts. The system must use two 3-inch diameter pulleys separated by a center distance between 4 and 6 inches. The design must also account for belt tension, shaft strength, journal bearing performance, and structural support.

The design process involves calculating the forces created by the belt, determining the required dimensions of the belt and shafts, selecting suitable bearing materials, and designing a supporting frame that can withstand the operating loads.

The final design will use engineering calculations and CAD analysis to verify that each component satisfies the required minimum factor of safety of 3.

## Analyze

The following table lists the initial design specifications selected for the pulley system. These values establish the operating conditions, material selections, and dimensional constraints that will be used throughout the design process.
Design Specification: 

| Parameter | Selected Value | Units |
|---|---:|---|
| Pulley diameter | 3.000 | in |
| Pulley radius | 1.500 | in |
| Center distance | 5.000 | in |
| Operating speed | 1,500 | RPM |
| Initial static belt tension | 5.000 | lbf |
| Belt material | Polyurethane rubber | -- |
| Belt yield strength | 471 | psi |
| Minimum safety factor | 3 | -- |
| Shaft material | 1060 hardened steel | -- |
| Pulley material | Aluminum | -- |
| Frame material | Steel | -- |

The following table identifies the known values and unknown variables required to design the polyurethane belt. The known values are used to calculate the tight-side and loose-side tensions, required belt cross-sectional area, minimum belt diameter, and overall belt length.

Belt Design Knowns/ Unknowns: 

| Variable | Description | Value | Units |
|---|---|---:|---|
| D | Pulley diameter | 3.000 | in |
| r | Pulley radius | 1.500 | in |
| C | Center distance | 5.000 | in |
| N | Rotational speed | 1,500 | RPM |
| T0 | Initial belt tension | 5.000 | lbf |
| Sy | Belt yield strength | 471 | psi |
| SF | Safety factor | 3 | -- |
| T1 | Tight-side tension | TBD | lbf |
| T2 | Loose-side tension | TBD | lbf |
| A | Required belt area | TBD | in^2 |
| d | Required belt diameter | TBD | in |
| L | Belt circumference | 19.425 | in |

<img width="550" height="1160" alt="image" src="https://github.com/user-attachments/assets/7ab2c805-d894-43a5-9c88-1ad24d72587c" />

The following table identifies the material properties and operating conditions needed to determine the minimum shaft diameter. These values will be used to calculate the torsional stress, allowable shear stress, and minimum cross-sectional area required to safely transmit power from the pulley.

Shaft Design

| Variable | Description | Value | Units |
|---|---|---:|---|
| Material | Shaft material | 1060 hardened steel | -- |
| N | Rotational speed | 1,500 | RPM |
| r | Pulley radius | 1.500 | in |
| T | Applied torque | TBD | lbf-in |
| Sy | Steel yield strength | TBD | psi |
| SF | Safety factor | 3 | -- |
| tau_allow | Allowable shear stress | TBD | psi |
| d_min | Minimum shaft diameter | TBD | in |
| A_min | Minimum shaft area | TBD | in^2 | 

The following table identifies the parameters required to select suitable journal bearings. The calculated shaft diameter, rotational speed, and bearing reaction forces will be used to determine bearing pressure, surface velocity, and the pressure-velocity (PV) rating. These results will be compared against the material limitations listed in Machinery's Handbook.

Jornal Bearings: 

| Variable | Description | Value | Units |
|---|---|---:|---|
| N | Shaft speed | 1,500 | RPM |
| D | Shaft diameter | TBD | in |
| L | Bearing length | TBD | in |
| W | Radial load per bearing | TBD | lbf |
| P | Bearing pressure | TBD | psi |
| V | Surface velocity | TBD | ft/min |
| PV | Pressure-velocity rating | TBD | psi-ft/min |
| Material | Selected bearing material | TBD | -- |

The following table outlines the preliminary dimensions and material selection for the supporting frame. These values will establish the initial CAD model. Creo Simulate will be used to evaluate the frame's maximum von Mises stress, displacement, and factor of safety under the calculated operating loads.

Frame Designs: 

| Parameter | Proposed Value | Units |
|---|---:|---|
| Base plate length | 10 | in |
| Base plate width | 10 | in |
| Frame material | Steel | -- |
| Bearing quantity | 4 | -- |
| Support plate quantity | 2 | -- |
| Mounting plate thickness | TBD | in |
| Maximum von Mises stress | TBD | psi |
| Maximum displacement | TBD | in |
| Minimum factor of safety | 3 | -- |

<img width="3024" height="4032" alt="Image_261104_220322" src="https://github.com/user-attachments/assets/2f72e56a-7886-48f2-863a-6c0b475ab51e" />

<img width="3024" height="4032" alt="Image_261104_220507" src="https://github.com/user-attachments/assets/ef37940f-0d75-44b5-a995-abffe8bcb354" />


## Engineering Lessons Learned: 

Through this project, I learned how multiple mechanical components work together to transfer rotational power. The design process required me to consider how belt tension, shaft torque, bearing loads, and frame strength affect one another.

One important lesson was understanding how the difference between tight-side and loose-side belt tension creates torque. Although both sides of the belt carry tension, the difference between the two forces is what produces the rotational torque at the pulley. This helped me understand why belt tension must be considered when designing a power transmission system.

I also learned that shaft diameter cannot be selected based on torque alone without considering the material properties and applied stresses. The strength of 1060 hardened steel determines how much torque the shaft can safely transmit before reaching its allowable stress. Applying a factor of safety ensures that the shaft is not designed directly at its material failure limit.

Another lesson was understanding that journal bearing selection involves more than choosing a bearing that fits around the shaft. Bearing pressure, surface velocity, and the pressure-velocity (PV) rating must all be considered. A bearing can have the correct dimensions but still be unsuitable if the material cannot withstand the operating pressure and sliding velocity.

During the frame design process, I learned how important alignment and structural stiffness are in rotating machinery. If the support plates deform or the shafts become misaligned, the belt may track incorrectly and place additional loads on the bearings. Using Creo Simulate provides a way to identify high-stress regions and areas of excessive displacement before manufacturing the frame.

Finally, I learned that mechanical design is an iterative process. Changing one component can affect the dimensions, forces, and performance requirements of other components. Completing the belt, shaft, and bearing calculations before finalizing the frame helps ensure that the entire assembly is designed around consistent operating conditions rather than treating each component as an independent part.

## Communicate

