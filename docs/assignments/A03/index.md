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

Finished product:
With the parametric CAD model completed, I was able to move on to the FEA portion of the project. The analytical calculation provided my expected deflection, while the FEA would allow me to verify whether the CAD model produced a similar result under the same loading conditions. The following photo shows the final design of the circular bar in Creo before I added the load and created the FEA setup. At this point, the geometry and dimensions of the bar were complete and based on my calculated design specifications.

<img width="1278" height="770" alt="image" src="https://github.com/user-attachments/assets/b07738a6-6c63-4b03-aa7c-2c8cdee42c29" />

## Deflection and von Mises Stress maps

