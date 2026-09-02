# A2 – Truss Stress Analysis

## Objective
The goal of this project is to design a lightweight planar truss that can support the applied 20–30 kN force while satisfying the given geometric and design constraints. From Figure 1, point B is a roller support, which provides only a vertical (Y-direction) reaction force. Point A is a pin support, which can provide both horizontal (X-direction) and vertical (Y-direction) reaction forces.

The geometry of the truss can also be determined from Figure 1. The distance from B to C is 0.3 m. Because the truss is symmetrical, the corresponding distance from A to D is also 0.3 m. The total distance from A to B is 1.2 m, which is divided into three 0.4 m sections.

These dimensions establish the basic geometry that will be used for the free-body diagram and the member-force analysis. Since there is no external horizontal force applied to the truss, the horizontal reaction at the pin support can be determined to be sum of A_x = 0 using the equilibrium equation sum of F_x = 0).

<img width="321" height="219" alt="image" src="https://github.com/user-attachments/assets/b769834a-e51c-428f-ac6b-9339e93ab634" />

# My Design Choice: 
I chose to use an upside-down trapezoid with a beam stretching from Point C to Point A as a supporting member. I chose this geometry because the additional member provides another connection between the upper and lower portions of the truss and gives the structure additional support. I then analyzed the truss to determine the forces in each member and verify how the chosen design responds to the applied loads.

<img width="2574" height="1306" alt="IMG_1431" src="https://github.com/user-attachments/assets/5663c75c-d63b-4c29-a492-ccb02bf2e727" />


## Analyze
The horizontal and vertical dimensions of the truss are given, which allows the diagonal member lengths to be calculated using the Pythagorean theorem. For the diagonal members with a horizontal distance of 0.4 m and a vertical distance of 0.3 m, the length can be found using L=sqrt{x^2+y^2}, giving a length of 0.5 m. These dimensions also allow the angles of the diagonal members to be determined, which are needed to break the member forces into their horizontal and vertical components.

I started the analysis at Joint D because the joint had one known force, the 25 kN applied load, and only two unknown member forces. Additionally, the truss is symmetrical, so the force in the corresponding member on the opposite side could be used as a check. This made Joint D the simplest point to begin the analysis and allowed me to use the results to solve the remaining joints more efficiently.

I then moved from Joint D to Joint C, followed by Joint B and finally Joint A. By solving the joints in this order, each step provided known forces that could be used in the next joint's free-body diagram. This allowed me to determine all of the internal member forces while also using the symmetry of the truss to verify my results.

The following picture shows the complete free-body diagrams (FBDs) and the corresponding equilibrium equations used to analyze each joint of the truss.

<img width="3024" height="4032" alt="IMG_1430" src="https://github.com/user-attachments/assets/975a1852-225f-4399-a1cd-fca1bd779619" />

## Cross-Sectional Area and Truss Weight
The yield strength and density used in the calculations were obtained from the material properties listed for ASTM A500 structural steel. The material data used was a yield strength of 290 MPa and a density of 7800 kg/m³. The source for these material properties is https://www.beamdimensions.com/materials/Steel/ASTM/ASTM_A500/

<img width="1480" height="146" alt="Screenshot 2026-09-01 210733" src="https://github.com/user-attachments/assets/15cc9e70-9162-4579-8bea-76c6f038f39b" />

The largest internal force in the truss is 41.67 kN, which occurs in members AD and BC. I used this maximum force to determine the required cross-sectional area for all members, providing a conservative design because every member will have an area capable of supporting the largest calculated force. A safety factor of 3.5 was applied to the yield strength of the A500 structural steel to determine the allowable stress.

The following image shows my calculations for parts i–iv, including the knowns and unknowns, symbolic solution, numerical cross-sectional area, and approximate truss weight.

<img width="3024" height="4032" alt="Image_260901_212508" src="https://github.com/user-attachments/assets/b21adbba-5a2c-4f45-9f71-5b4653cc5f75" />

## Connecting Pin Design

The largest reaction load from the truss analysis is 25 kN. The connecting pins are made from hardened tool steel with a yield shear strength of 170 ksi and a density of 0.278 lb/in³. A safety factor of 4 is required, and the minimum cross-sectional area of the pins is the primary unknown.

The pin at the support was selected for the FBD because it experiences the largest reaction load of 25 kN. Since the connection is designed as a single-shear connection, the applied reaction produces one shear plane through the pin. This shear force is used to determine the minimum required cross-sectional area.

The calculated minimum pin diameter was 0.410 in. A 7/16 in. diameter pin was selected as the practical design size because it is larger than the calculated minimum and provides an additional margin above the required shear area.
## Decide
_Which geometry did you select, and why? This is your first open design choice in the course — defend it._

## Communicate

