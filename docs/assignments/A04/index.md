# A4 Motor Mount

## Overview

The objective of this project was to design a motor mount for a brushed 24 V DC gear motor. The mount was designed as two main features: Feature 1 attaches to the motor, while Feature 2 attaches to a rigid wall. Both features were analyzed as cantilever beams using bending stress and deflection equations. A safety factor of 3 was used to account for the required loading conditions and holes in the motor-mounted feature.

Design Requirements
Applied load: 300 N
Safety factor: 3
Maximum allowable deflection: 0.30 mm
Material: PLA
Feature 1 length: 50 mm
Feature 2 dimensions: 50 mm × 50 mm
Bolt clearance holes: Ø3.4 mm
Motor shaft clearance hole: Ø6.5 mm

<img width="2284" height="2712" alt="IMG_1552 (1)" src="https://github.com/user-attachments/assets/0b025448-4e9b-4220-b1a1-255d331285ba" />

## Final Feature 1 Geometry

Using the calculated stress and deflection requirements, the final cross-sectional geometry for Feature 1 was selected. The motor-attached feature was modeled as a rectangular section with a 50 mm length, 50 mm width, and the same plate thickness used throughout the motor mount. The 50 mm length was used as the cantilever length in the beam analysis, while the final plate thickness was selected based on the completed CAD design. The motor shaft and screw clearance holes were included in the CAD model, with the safety factor accounting for the reduction in cross-sectional area caused by these holes.

## Feature 2 Geometry

The final Feature 2 geometry uses a 50 mm × 50 mm cross section and a 50 mm length for the cantilever analysis. The calculated maximum bending stress was 0.72 MPa, which is below the allowable stress of 15.93 MPa when using the required safety factor of 3.

The calculated maximum deflection was 0.0081 mm, which is also below the maximum allowable deflection of 0.30 mm. Four 3.4 mm clearance holes were included in the wall attachment feature to allow the motor mount to be fastened to the rigid wall.

1. Purpose of Feature 2

Feature 2 is the section of the motor mount that connects the mount to the rigid wall. This feature needs to support the load transferred from the motor while keeping the mount from bending excessively. I treated the wall connection as a fixed support because the assignment states that the wall is rigid.

2. Initial Design / Approach
   
To determine the required size of Feature 2, I modeled the feature as a cantilever beam. This approach represents the wall as the fixed end of the beam and the motor load as a force acting away from the wall. I used the beam bending equations to check both the strength of the material and the amount of deflection.

<img width="1280" height="1249" alt="IMG_1574" src="https://github.com/user-attachments/assets/de42fa64-618b-4862-99ed-62bc085156b6" />

The free-body diagram shows the loading condition used for the analysis. The 300 N load represents the design load applied to the motor mount, while the 50 mm dimensions represent the geometry used in the beam calculation.

3. Material Selection

I selected PLA as the material for the motor mount. The material properties were used to determine whether the selected geometry could withstand the applied load while maintaining the required safety factor. The yield strength was used for the stress check, while the modulus of elasticity was used to evaluate deflection.

You don't need to repeat all the material numbers here because they're already visible in your calculation image.

4. Geometry Selection

I used a 50 mm length and a 50 mm by 50 mm rectangular cross section for Feature 2. This geometry provides a large cross-sectional area and moment of inertia, which helps reduce bending stress and deflection. The dimensions were then incorporated into the CAD model so that the analytical design and physical model matched.

<img width="1024" height="2032" alt="Image_260917_002805" src="https://github.com/user-attachments/assets/fdf39fe1-0f48-49b6-9614-af7455e5edc6" />

5. Results

The beam analysis showed that the selected Feature 2 geometry satisfies both the strength and deflection requirements. The calculated bending stress was below the allowable stress after applying the required safety factor. The calculated deflection was also below the maximum allowable deflection of 0.30 mm. Based on these results, I used the selected geometry in the final motor mount.

6. Connection to the Wall

Four clearance holes were added to Feature 2 so the motor mount can be fastened to the rigid wall using bolts. The holes were modeled as 3.4 mm clearance holes as specified by the assignment. I kept the holes as clearance holes rather than adding threads because the bolts are supported by the rigid wall rather than being threaded directly into the printed part.

7. Transition to Final CAD

Finish by connecting the analysis to what you actually built:

After completing the beam analysis, I used the calculated geometry to create Feature 2 in Creo. The final model includes the wall mounting holes and the geometry needed to connect Feature 2 to the rest of the motor mount. This allowed the analytical design to be carried into the final CAD model.

## Section 3 — Engineering Drawing + Extra section

<img width="1266" height="962" alt="image" src="https://github.com/user-attachments/assets/f850ff48-dccd-4c64-8847-b5b10794714c" />

After completing the CAD model, I created an engineering drawing to communicate the final geometry of the motor mount. Multiple orthographic views were used so that the important dimensions and features could be shown without relying only on the 3D model. The side view shows the overall L-shaped geometry and the 50 mm dimensions of the vertical and horizontal sections, while the other views show the motor opening, shaft opening, and wall mounting holes.

The motor mounting feature includes a Ø28 mm opening and a Ø6.5 mm center hole. The wall attachment includes four Ø3.4 mm clearance holes for the mounting bolts. These holes were modeled as clearance holes because the bolts pass through the motor mount and attach it to the rigid wall.

The isometric view was included to give an overall representation of the finished part, while the orthographic views provide the dimensions and feature locations needed to manufacture the part. I used the drawing to verify that the geometry created in Creo was represented correctly and that the major dimensions and hole sizes were communicated.
<img width="1024" height="1032" alt="Image_260917_003413" src="https://github.com/user-attachments/assets/12e91020-9dd0-4160-96b9-55115ab0a7db" />

Drawing File: 
 [mmd.drw.zip](https://github.com/user-attachments/files/32319731/mmd.drw.zip)
 
Part File: 
 [motor_mount.prt.zip](https://github.com/user-attachments/files/32319758/motor_mount.prt.zip)

## Section 4 3D CAD model of the motor mount.

<img width="1246" height="978" alt="image" src="https://github.com/user-attachments/assets/1b65fa75-0425-4f4b-8878-4f8528aec4cc" />
