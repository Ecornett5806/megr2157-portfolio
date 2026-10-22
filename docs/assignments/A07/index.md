## FEA Design Comparison - A7

| FEA Parameter | Design I (Original) | Design II | Design III |
|---|---:|---:|---:|
| Maximum stress (ksi) | 74 | 67.32 | 43 |
| Location of maximum stress | Base of cylinder | Base of cylinder | Base of cylinder* |
| Maximum deflection (in) | 1.2655 × 10⁻³ | 5.6663 × 10⁻⁴ | 2.07 × 10⁻⁴ |
| Location of maximum deflection | End of cylinder | End of cylinder | End of cylinder* |
| Mass (kg) | 0.0073 | 0.067311* | 0.00304 |
| Safety factor | 0.52 | 0.535 | 0.837 |
| Number of elements | 2,029 | 3,674 | 2,533 |

## Design Requirements

| Parameter | Required Value |
|---|---:|
| Applied load | 700 lbf |
| Material | ASTM A36 steel |
| Yield strength | 36 ksi |
| Allowable stress (safety factor of 4) | 9 ksi |
| Maximum feature deflection | 0.005 in |
| Required safety factor | 4 |

Imiges of #1 

<img width="2560" height="1440" alt="Screenshot (2)" src="https://github.com/user-attachments/assets/6495e09a-0c91-41fa-aa65-9297d4ce000c" />

<img width="2560" height="1440" alt="Screenshot (1)" src="https://github.com/user-attachments/assets/d4cb904b-f623-4910-a6f4-6d5b66412da7" />

#2:
<img width="2560" height="1440" alt="Screenshot (3)" src="https://github.com/user-attachments/assets/4b3953e8-aa8a-41f1-b941-fa397e0d487f" />

<img width="2560" height="1440" alt="Screenshot (4)" src="https://github.com/user-attachments/assets/30b5100f-f189-4fa8-ad6d-21c0199ea7a1" />

#3:

<img width="2560" height="1440" alt="Screenshot (5)" src="https://github.com/user-attachments/assets/e6b94658-dcf8-4dd2-b386-921df8061d7c" />

<img width="2560" height="1440" alt="Screenshot (6)" src="https://github.com/user-attachments/assets/5ca4eecc-cf7e-46e5-b7eb-4b41c23c1d27" />

## Results and Discussion

Design III reduced the maximum stress from 74 ksi to 43 ksi, a reduction of approximately 41.9%. Maximum deflection decreased from 1.2655 × 10⁻³ in to 2.07 × 10⁻⁴ in, a reduction of approximately 83.6%. The reported mass decreased from 0.0073 kg for Design I to 0.00304 kg for Design III.

Although Design III improved stress, deflection, and reported mass, its maximum stress of 43 ksi remains above the allowable stress of 9 ksi. Its estimated safety factor is approximately 0.84, below the required safety factor of 4. Therefore, Design III improved the simulated performance of the original bracket but did not meet the strength requirement.

## Analysis of Stress Reduction Limitations

The maximum stress was difficult to reduce because it consistently occurred at the base of the cylinder, where the applied load transferred into the bracket's base. This area experiences concentrated stresses due to the geometry and the bending forces acting on the cylinder. Although increasing the cylinder diameter and modifying the rounded connection improved the results, these changes did not eliminate the stress concentration. Adding ribs and hollowing the cylinder also changed how the load traveled through the part, sometimes increasing the maximum stress rather than reducing it.

The original bracket geometry limited how much material could be added or removed without affecting its function, stiffness, and mass. Additionally, the maximum stress can be sensitive to mesh refinement and local geometric features, so the results must be checked for convergence before comparing designs. Design III reduced maximum stress from 74 ksi to 43 ksi, but this remained above the 9 ksi allowable stress required for a safety factor of 4. The iterations demonstrated that improving a design requires balancing stress, deflection, mass, and geometry rather than assuming that adding material or increasing a fillet will always improve performance.

# Mechanical Linkage Link — FEA Design Optimization

## Project Overview

The purpose of this project was to reduce the mass of a small mechanical linkage link while maintaining sufficient strength and stiffness. The original component had a shape similar to a soda-can tab, with rounded ends and holes for connecting pins.

I created three design iterations in Creo and used Finite Element Analysis (FEA) to evaluate the effects of each geometry change. Design I served as the baseline, Design II reduced the link's thickness, and Design III added rounds around the holes.

## Design Objectives

- Reduce the overall mass of the link.
- Maintain sufficient strength under the applied loading.
- Evaluate maximum stress and deformation for each design.
- Compare safety factors and mesh element counts.
- Use FEA results to assess the effects of each design change.

## Design I — Original Link

<img width="2560" height="1440" alt="Screenshot (14)" src="https://github.com/user-attachments/assets/37e02838-58ac-47d4-befe-14b60f2d1d5b" />

<img width="2560" height="1440" alt="Screenshot (7)" src="https://github.com/user-attachments/assets/79e8e3f4-1127-4597-a503-9b85bad486a0" />

<img width="2560" height="1440" alt="Screenshot (8)" src="https://github.com/user-attachments/assets/a5fff523-51e1-4bab-a8b6-4dbb484ec570" />

### Design Description

Design I was the original link geometry. It had rounded ends and holes for connecting pins. I used this design as the baseline for comparing the changes made in the next two iterations.

### FEA Results

| Measurement | Result |
|---|---:|
| Weight | 0.18000 lb |
| Maximum Stress | 32 MPa |
| Maximum Deformation | 0.000044053 in |
| Number of Elements | 389 |
| Estimated Safety Factor | 7.81 |

The safety factor was estimated using an assumed low-carbon steel yield strength of 250 MPa.

### Design Evaluation

Design I established the baseline values for the optimization process. Its weight was 0.18 lb, and its maximum reported stress was 32 MPa. These values were used to evaluate the effect of reducing material in the later designs.

**Images to include:**
- Original CAD model
- Original dimensions
- FEA stress plot
- FEA deformation plot

## Design II — Reduced Thickness

### Design Description

For Design II, I reduced the link's thickness by approximately half while keeping the rounded ends and pin-hole locations unchanged. The purpose was to reduce the amount of material used and decrease the overall weight.

### FEA Results

| Measurement | Result |
|---|---:|
| Weight | 0.09623 lb |
| Maximum Stress | 44 MPa |
| Maximum Deformation | 0.000023631 in |
| Number of Elements | 735 |
| Estimated Safety Factor | 5.68 |

### Design Evaluation

Reducing the thickness decreased the weight from 0.18 lb to 0.09623 lb, a reduction of approximately 46.54%. Maximum stress increased from 32 MPa to 44 MPa, while the reported maximum deformation decreased.

The estimated safety factor decreased from 7.81 to 5.68. This indicated a trade-off between reducing material and maintaining structural performance.

The decrease in deformation was unexpected after a substantial reduction in thickness. I would verify that both simulations used the same loading, constraints, units, and deformation result type before drawing a final conclusion.

<img width="2560" height="1440" alt="Screenshot (16)" src="https://github.com/user-attachments/assets/0c8e36b9-6197-434a-bcef-52b7ad3bb0fe" />

<img width="2560" height="1440" alt="Screenshot (15)" src="https://github.com/user-attachments/assets/12ad04f8-7281-4a61-9c96-6944b38b3b66" />

<img width="2560" height="1440" alt="Screenshot (13)" src="https://github.com/user-attachments/assets/8d69a84b-bef2-446e-bbf8-bba7d03c8f71" />


## Design III — Rounded Hole Edges

### Design Description

For Design III, I added 0.4-inch rounds around the holes while retaining the reduced thickness from Design II. The purpose was to evaluate the effect of the revised hole geometry on stress, deformation, and weight.

### FEA Results

| Measurement | Result |
|---|---:|
| Weight | 0.09534 lb |
| Maximum Stress | 50 MPa |
| Maximum Deformation | 0.000031586 in |
| Number of Elements | 9,151 |
| Estimated Safety Factor | 5.00 |

The estimated safety factor was calculated as:

### Design Evaluation

Design III was the lightest of the three designs. Its weight decreased from 0.09623 lb in Design II to 0.09534 lb. However, the maximum stress increased to 50 MPa, and the reported deformation increased compared with Design II.

The estimated safety factor was 5.00 using the assumed yield strength of 250 MPa. These results demonstrate that reducing mass does not necessarily improve every aspect of structural performance.

The mesh contained 9,151 elements, considerably more than the previous designs. This difference may reflect changes in mesh density or geometry. Mesh convergence should be verified before making a definitive comparison of maximum stress and deformation.


## Comparison of All Three Designs

| Measurement | Design I | Design II | Design III |
|---|---:|---:|---:|
| Weight (lb) | 0.18000 | 0.09623 | 0.09534 |
| Maximum Stress (MPa) | 32 | 44 | 50 |
| Maximum Deformation (in) | 0.000044053 | 0.000023631 | 0.000031586 |
| Number of Elements | 389 | 735 | 9,151 |
| Estimated Safety Factor | 7.81 | 5.68 | 5.00 |

## Mass Reduction Calculations

The percentage reduction in weight was calculated relative to Design I.

### Design II

Design II reduced the original weight by approximately 46.54%.

### Design III

<img width="2560" height="1440" alt="Screenshot (10)" src="https://github.com/user-attachments/assets/19ffbf30-4e3a-4a05-ab6c-4e87395ba10a" />

<img width="2560" height="1440" alt="Screenshot (11)" src="https://github.com/user-attachments/assets/543f4a7f-222c-467b-ae4e-b9e778ff01d3" />

<img width="2560" height="1440" alt="Screenshot (12)" src="https://github.com/user-attachments/assets/27eb24f9-ede6-4c84-81f4-e24a0ebd41a7" />


Design III reduced the original weight by approximately 47.03%.

The additional reduction from Design II to Design III was 0.00089 lb.

## Lessons Learned

This project showed me that removing material can significantly reduce a component's weight, but it can also increase stress and affect deformation. Reducing the thickness in Design II produced the largest weight reduction. Adding rounds around the holes in Design III produced a smaller additional weight reduction, while maximum stress increased.

I also learned that FEA results must be compared carefully. A higher number of elements does not automatically mean a simulation is more accurate. Mesh refinement and convergence need to be checked to determine whether stress and deformation results are sufficiently stable.

Another lesson was the importance of making controlled design changes. By changing the geometry in stages, I could compare each iteration and better understand the trade-offs between weight and structural performance.

## Final Conclusion

The final design reduced the reported weight from 0.18 lb to 0.09534 lb, an overall reduction of approximately 47.03%. However, maximum stress increased from 32 MPa to 50 MPa across the three designs.

Design III was the lightest option, but the final design should not be selected based on weight alone. The actual material yield strength, required safety factor, deformation limit, pin fit, and mesh convergence must be verified before concluding that the design meets all engineering requirements.

## Time Log

| Activity | Time |
|---|---:|

| **Total Time** | 13 hrs |

## Resources Used

- Creo for CAD modeling and Finite Element Analysis.
- Low-carbon steel material properties assigned in Creo.
- FEA stress and deformation plots.
- CAD dimensions and mass properties for each design iteration.

## CAD File

Both Files are In the ZIP 

[bp3.prt.zip](https://github.com/user-attachments/files/33798076/bp3.prt.zip)
