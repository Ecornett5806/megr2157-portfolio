# A3 – Parametric and FEA

## Brainstorming/ Design Specs 
Calculating and design choices:

I first selected a diameter of 0.25 inches for the circular bar. I chose this as a reasonable starting cross-sectional size before determining the required length. Using the area equation for a circle, I calculated the cross-sectional area to be 0.0491 in². This area was then used in the direct tension elongation equation to determine the required length of the bar.

After determining the cross-sectional area, I used the direct tension elongation equation from Machinery's Handbook to determine the required length of the bar. The equation relates the applied load, bar length, cross-sectional area, material stiffness, and resulting deflection. Because I needed to determine the length, I rearranged the equation:For my initial design, I selected a load of 400 lbf, a Young's Modulus of \(10\times10^6\) psi, and a maximum allowable deflection of 0.009 in. Using the cross-sectional area calculated in the previous section:This calculation gave me an initial bar length of approximately 11.05 in. I then used this result as the basis for creating the bar parametrically in Creo.
## Units Creo was in 

Before creating the model, I verified that Creo was using the appropriate unit system for my calculations. I used inches for length, lbf for force, and psi for stress/modulus values so that the units matched my calculations.

<img width="378" height="48" alt="image" src="https://github.com/user-attachments/assets/0f0367cf-aabc-4bf0-9580-a6a302a92c41" />
Load: 400 lbf
Young's Modulus: (10(10^6))psi
Maximum deflection: 0.009 in
Diameter: 0.25 in
Cross-sectional area: 0.0491 in²
Calculated length: approximately 11.05 in

## Calculated Design Specs on paper:

<img width="3024" height="4032" alt="Image_260907_135748" src="https://github.com/user-attachments/assets/861390f9-1ffc-49b1-a9a8-24816b8ee26b" />

## design specs in CAD using Parameters and Relations:

With the initial dimensions and required length determined, I moved into Creo to create the bar as a parametric model. Instead of manually entering the calculated length, I created parameters and relations that allowed Creo to calculate the length from the design inputs.

This made the model more flexible because the design could be changed by modifying the input parameters rather than manually recalculating and changing individual dimensions. This also allowed me to see how changing one design variable affected the required length of the bar.

<img width="400" height="58" alt="image" src="https://github.com/user-attachments/assets/a0961a24-d87a-4882-89da-765e64f412f7" />

<img width="468" height="202" alt="image" src="https://github.com/user-attachments/assets/c648e09c-8de3-44fb-aace-4edda4fa4868" />

<img width="460" height="126" alt="image" src="https://github.com/user-attachments/assets/38318eea-1be3-4aa5-972b-b3512f2fae3c" />

## Relations: 

I then connected the Creo model dimensions to the parameters using relations. The diameter of the circular cross section was linked to the DIAMETER parameter, while the extrusion length was linked to the calculated BAR_LENGTH parameter.

The main relations were:

d18 = DIAMETER
AREA = PI*DIAMETER^2/4
BAR_LENGTH = MAX_DEFLECTION*AREA*MODULUS/LOAD
d19 = BAR_LENGTH

This allowed Creo to automatically calculate the required bar length based on the design inputs.

<img width="696" height="358" alt="image" src="https://github.com/user-attachments/assets/6e8baa0e-7bd9-43fb-ba1e-e583bc136fbd" />

## Finished product:

With the parametric CAD model completed, I was able to move on to the FEA portion of the project. The analytical calculation provided my expected deflection, while the FEA would allow me to verify whether the CAD model produced a similar result under the same loading conditions. The following photo shows the final design of the circular bar in Creo before I added the load and created the FEA setup. At this point, the geometry and dimensions of the bar were complete and based on my calculated design specifications.

<img width="1278" height="770" alt="image" src="https://github.com/user-attachments/assets/b07738a6-6c63-4b03-aa7c-2c8cdee42c29" />

## Deflection and von Mises Stress maps

After completing the parametric design of the circular bar, I used Creo's Structure Simulation to verify the design through finite element analysis (FEA). I used the same loading condition that was used to determine the bar's geometry: a 400 lbf distributed axial load applied to one end of the bar, with the opposite end constrained.

The purpose of the FEA was to compare the actual behavior of the CAD model with the results predicted by my direct-tension calculations. This allowed me to verify both the bar's maximum deflection and Von Mises stress.

 ## von Mises Stress Graph:
 
 <img width="1658" height="952" alt="Screenshot 2026-09-07 194857" src="https://github.com/user-attachments/assets/8fed1cf9-0d93-4df0-b965-08c1e1cc96e6" />
The maximum Von Mises stress from the FEA was approximately 8603psi or 8.60 ksi

For comparison, the theoretical axial stress from my calculation was approximately: 400/0.0491 = 8147 psi or approximately 8.15 ksi.

The FEA result of 8.60 ksi is reasonably close to the theoretical value of 8.15 ksi. The difference is approximately 5.6%. Since this is a simple uniform bar under direct tension, the stress is relatively consistent along the length of the bar.

## Deflection Graph: 

I then generated a displacement map to determine the maximum deflection of the bar under the 400 lbf load.

<img width="1654" height="888" alt="Screenshot 2026-09-07 194912" src="https://github.com/user-attachments/assets/592dfb2d-e6e9-47a6-b1fa-c52b0e955301" />

The FEA produced a maximum displacement of approximately 0.008912 in

My analytical design was based on a maximum allowable deflection of 0.009 in

The FEA result is slightly below the maximum allowable deflection. The difference between the FEA result and the design limit is:

0.009-0.008912= 0.000088 in 

This shows that the bar meets the maximum deflection requirement. The close agreement between the analytical calculation and FEA also gives me confidence that the parametric model, material properties, loading, and constraints were set up correctly.

## FOS calculation: 

given the S_y=40 ksi we can use the formula N=s_y/σ_maxto find the Factor of Safety where S_Y=40ksi and σ_max= 8.60 ksi. 
so 40/8.60= 4.65 

The resulting factor of safety is approximately 4.65. This means the yield strength of the aluminum is approximately 4.65 times greater than the maximum Von Mises stress predicted by the FEA.

Overall, the FEA verified that my circular bar design meets the specified deflection and strength requirements under the 400 lbf distributed axial load. The maximum displacement was 0.008912 in, which is below the 0.009 in maximum allowable deflection, and the maximum Von Mises stress was 8.60 ksi, which is below the aluminum yield strength of 40 ksi. The calculated factor of safety was 4.65.

The FEA results were also reasonably close to my analytical calculations, which helped confirm that the parametric design, material properties, loading, and constraints were set up correctly.

Here are my hand calculations for the above section: 

<img width="2696" height="696" alt="IMG_1468" src="https://github.com/user-attachments/assets/9c00e1c3-3f04-488f-816e-9e0db1b1d5ad" />

## The design Reflection: 

Given my analytical maximum deflection of 0.009000 in and my FEA maximum displacement of 0.008912 in, I calculated the percent difference between the two results. The percent difference came out to approximately 0.98%.

I calculated the percent difference by finding the difference between the two values, dividing that difference by the analytical value of 0.009000 in, and then multiplying by 100. This small percent difference shows that the analytical calculation and FEA result are very close to one another.

The close agreement is expected because the bar has a simple geometry and is primarily subjected to axial loading. The hand calculation assumes a uniform cross-section and axial loading, which closely matches the conditions used in the FEA model. Since there are no major geometric discontinuities or stress concentrations in the original bar, the FEA does not need to capture complicated local behavior. The mesh is therefore sufficient to accurately represent the overall deformation.

For this design, I would trust the FEA result slightly more because it accounts for the actual geometry and boundary conditions of the model. However, the hand calculation provides a useful check to make sure the FEA result is reasonable. The fact that the two results differ by only 0.98% gives confidence that the model and calculations are correct.

## Adding a Hole

For the hypothetical pin hole, I assumed a hole diameter of 0.125 in because a specific hole diameter was not provided. Since the bar width is 0.25 in, the ratio (d/W) is 0.50. Using Peterson's stress concentration chart for a flat bar with a circular hole in tension, the corresponding stress concentration factor is approximately (K_t = 2.16).

The hole is significant because its diameter is relatively large compared to the width of the bar. This removes a substantial portion of the material that would normally carry the applied load. The load must therefore redistribute around the hole, causing the stress to become concentrated near the edge of the opening. The stress concentration factor accounts for this increase in local stress and allows the peak stress at the hole to be estimated.

The calculations below show the allowable stress, estimated peak stress at the hole, and a comparison between the stresses with and without the hypothetical hole.

<img width="3021" height="953" alt="IMG_1472" src="https://github.com/user-attachments/assets/0a6fabc3-5a8e-48a7-b13f-7771cf6f18ac" />

The large change in stress is caused by the stress concentration created by the pin hole. Without the hole, the bar has a relatively uniform cross-section, allowing the load to be distributed more evenly throughout the material. When the hole is introduced, the load must flow around the opening, causing the stress to increase significantly near the edge of the hole. Therefore, the estimated peak stress at the hole is much higher than the nominal stress measured away from the hole in the original FEA model.

This demonstrates why features such as pin holes must be considered when evaluating the strength and safety of a mechanical component. Even when the overall nominal stress is relatively low, a geometric feature can create a much higher local stress that may become critical when compared to the material's allowable stress.

## Modify Design Parameters

For this design cycle, I changed the load to 200 lbf and increased the diameter to 1 in, while keeping the Young’s modulus the same. I predicted that the required length would increase because of the significantly larger diameter. After calculating the new design, the required cross-sectional area was 0.7854 in² and the required length was approximately 353.429 in.

## Pictures of both Graphs and the New A and Length: 

For this design cycle, I changed the load to 200 lbf and increased the diameter to 1 in, while keeping the Young’s modulus the same. I predicted that the required length would increase because of the significantly larger diameter. After calculating the new design, the required cross-sectional area was 0.7854 in² and the required length was approximately 353.429 in.

<img width="446" height="138" alt="Screenshot 2026-09-08 205719" src="https://github.com/user-attachments/assets/7b856fd6-5bf3-4e25-a3da-4c56e4b5828f" />

After determining the new area and length, I used these updated dimensions to run the FEA on the bar. I kept the aluminum material and fixture the same as the original design and applied the 200 lbf load.
<img width="1914" height="828" alt="Screenshot 2026-09-08 205912" src="https://github.com/user-attachments/assets/44ba6b62-c3ef-4c3d-89db-2ee73512a53b" />

The deflection map showed a maximum displacement of approximately 0.0182 in. This result allowed me to see how the change in the design parameters affected the bar's deformation under the applied load.

The Von Mises stress map showed a maximum stress of 543.9539 psi. I compared this value to the aluminum yield strength of 40 ksi to determine whether the bar would remain below the material's strength.

<img width="1866" height="910" alt="Screenshot 2026-09-08 205922" src="https://github.com/user-attachments/assets/0850e339-7eda-41ea-a49d-0228af713411" />

The Von Mises stress map showed a maximum stress of 543.9539 psi. I compared this value to the 40 ksi yield strength of aluminum and calculated the safety factor. The maximum stress was well below the yield strength, resulting in a safety factor of approximately 73.5. This shows that the bar remains below the yield strength of the aluminum under the applied load.

<img width="3021" height="1340" alt="IMG_1473" src="https://github.com/user-attachments/assets/59a29217-7349-43da-afd2-d3cfd19dd770" />

## My Mistakes:

One mistake I made during this project was initially being unsure about the units in Creo. I was using inches and lbf for my calculations, but I was confused when I did not see PSI listed as a separate unit option. I learned that the IPS unit system is still compatible with psi, since pressure/stress is expressed as lbf/in².

Another mistake I made was entering some of the parameter information incorrectly in the Creo Relations window. I initially tried to enter parameter values directly into the relations instead of setting the values in the Parameters window. I learned that the parameters should be defined first, and the Relations window should be used to connect those parameters to equations and model dimensions.

I also had some difficulty identifying the correct dimension symbols in Creo. I had to determine which dimension controlled the circle diameter and which controlled the extrusion length. I eventually identified d18 as the diameter dimension and d19 as the extrusion depth and connected them to my parameters.

Another issue I encountered was the small difference between my hand calculation and the value displayed by Creo. My hand calculation gave approximately 11.05 in, while Creo displayed approximately 11.04 in. I initially thought this was an error, but I learned that the difference came from rounding. Creo was using the more precise value of the circular area rather than my rounded value of 0.0491 in².

During the FEA setup, I also initially had the force components set incorrectly. I had values of 200 lbf in the X, Y, and Z directions, which did not represent the 400 lbf axial load from my design calculation. I corrected this by using a 400 lbf total force and applying it in the axial direction.

I also initially questioned whether an axial force was correct because the assignment showed the load as being distributed. I learned that axial describes the direction of the force, while distributed describes how the force is applied to the surface. For my model, the 400 lbf force was distributed across the circular end face while acting along the longitudinal axis of the bar.

Finally, I initially thought something was wrong with my Von Mises stress map because most of the bar appeared red/orange. I learned that the colors represent the stress range relative to the minimum and maximum values in the model. The numerical maximum stress was more important than the color itself. The FEA produced a maximum stress of approximately 8.60 ksi, which was below the aluminum yield strength of 40 ksi.

## What I learned:

This project helped me become more comfortable with parametric modeling and FEA in Creo. I learned that small setup details, such as units, parameter relationships, force direction, and how a load is distributed, can have a large effect on the analysis. I also learned the importance of checking FEA results against analytical calculations instead of assuming that the simulation is automatically correct. In this project, my analytical deflection was 0.009000 in and my FEA displacement was 0.008912 in, giving a difference of only approximately 0.98%. This comparison helped me understand how analytical calculations can be used to verify an FEA model.

## Time Spent: 
Overall, I spent approximately 9 hours working on this project from Sunday through the time of submission. The work was completed on and off rather than in one continuous session. A significant portion of the time was spent learning the Creo interface, troubleshooting mistakes, creating the parametric relations, setting up the FEA, and interpreting the results. So Approximate time spent ~9 hours.

