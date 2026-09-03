# A2 – Truss Stress Analysis

## Objective
The goal of this project is to design a lightweight planar truss that can support the applied 25 kN force while satisfying the given geometric and design constraints. From Figure 1, point B is a roller support, which provides only a vertical (Y-direction) reaction force. Point A is a pin support, which can provide both horizontal (X-direction) and vertical (Y-direction) reaction forces.

The geometry of the truss can also be determined from Figure 1. The distance from B to C is 0.3 m. Because the truss is symmetrical, the corresponding distance from A to D is also 0.3 m. The total distance from A to B is 1.2 m, which is divided into three 0.4 m sections.

These dimensions establish the basic geometry that will be used for the free-body diagram and the member-force analysis. Since there is no external horizontal force applied to the truss, the horizontal reaction at the pin support can be determined using ∑F_x=0 Giving A_X=0

<img width="321" height="219" alt="image" src="https://github.com/user-attachments/assets/b769834a-e51c-428f-ac6b-9339e93ab634" />

# My Design Choice: 
I chose to use an upside-down trapezoid with a beam stretching from Point C to Point A as a supporting member. I chose this geometry because the additional member provides another connection between the upper and lower portions of the truss and gives the structure additional support. I chose this geometry before completing the force analysis, so I then used the analysis to determine whether my initial design could actually support the applied load.

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

The largest internal force in the truss is 47.46 kN, which occurs in members AD and BC. I used this maximum force to determine the required cross-sectional area for all members, providing a conservative design because every member will have an area capable of supporting the largest calculated force. A safety factor of 3.5 was applied to the yield strength of the A500 structural steel to determine the allowable stress.

The following image shows my calculations for parts i–iv, including the knowns and unknowns, symbolic solution, numerical cross-sectional area, and approximate truss weight.

<img width="4284" height="5712" alt="IMG_1448" src="https://github.com/user-attachments/assets/4f1ceb02-e100-46fc-89db-2b598465aa81" />

<img width="3024" height="4032" alt="Image_260902_221903" src="https://github.com/user-attachments/assets/84807a9b-905b-4dae-b146-7cfc094b7394" />

## Connecting Pin Design

The largest force acting on a connecting pin from the truss analysis is 8.33 kN. The connecting pins are made from hardened tool steel with a yield shear strength of 170 ksi and a density of 0.278 lb/in³. A safety factor of 4 was applied to the yield shear strength to determine the allowable shear stress.

The pin with the largest calculated shear force was selected for the free-body diagram. Since the connection is designed as a single-shear connection, the pin experiences one shear plane. The calculated shear force was used to determine the minimum required cross-sectional area of the pin.

The minimum required pin area was calculated as 0.0441 in², which corresponds to a theoretical pin diameter of approximately 0.237 in. I selected a 1/4 in diameter pin as the practical design size because it is larger than the calculated minimum diameter and therefore provides additional capacity while remaining a relatively small and lightweight connection.

Finally, I determined the approximate combined weight of the two connecting pins using the selected 1/4 in diameter and the density of the hardened tool steel. The calculated combined mass of the pins was .027316 lb.

## Decide
Based on the results of the truss analysis, I selected the member dimensions and pin sizes that satisfy the required safety factors while keeping the structure as lightweight as practical. The largest internal member force was used to size the truss members, while the largest calculated pin force was used to determine the required pin diameter.

I selected the upside-down trapezoidal configuration because it was the design I initially wanted to investigate, and the analysis showed that it could support the applied 25 kN load while satisfying the required constraints. The final CAD model represents the truss members as one part and uses separate cylindrical pins at the connections.

<img width="1018" height="524" alt="Screenshot 2026-09-02 200613" src="https://github.com/user-attachments/assets/4dee0cce-d635-471a-a645-dbee8b25e685" />

Finally, I determined the approximate combined weight of the truss and connecting pins using the calculated member dimensions, the selected 1/4 in diameter pins, and the density of the materials. My hand calculations gave an approximate total weight of 15.45 kg, or 34.06 lb. This was a stark contrast to the CAD model, which predicted a mass of less than 1 kg. I believe the difference is mainly due to differences between my calculated dimensions and the geometry of my CAD model. The CAD model was created from my initial design and may contain dimensions or features that do not perfectly match the calculations I completed by hand. Additionally, I had to use low-carbon steel in Creo because A500 structural steel was not available, which introduces a difference in material properties. This comparison showed me how important it is to carefully verify dimensions, units, material properties, and geometry when transferring calculations into a CAD model.

<img width="744" height="288" alt="Screenshot 2026-09-02 164100" src="https://github.com/user-attachments/assets/43db6ae8-00b2-4b08-8073-c980869e1376" />

After completing the CAD model, I used the Mass Properties tool in Creo to determine the predicted weight of the truss. This allowed me to use the material density and the finalized geometry of the model to calculate its mass and weight. I then compared the CAD-predicted weight with my hand calculations to determine how closely the physical model matched my original calculations. This comparison also helped verify that the dimensions and material properties used in the CAD model were consistent with the design calculations.

Based on the results of the truss analysis, I selected the member dimensions and pin sizes that satisfy the required safety factors while keeping the structure as lightweight as practical. The largest internal member force was used to size the truss members, ensuring that all members have sufficient cross-sectional area to withstand the calculated loading. The connecting pins were similarly sized using the largest calculated pin force and a safety factor of 4.

For the overall geometry, I used an upside-down trapezoidal configuration with an additional member connecting the lower joints. This design provides a simple load path between the members while maintaining the geometric constraints given in the problem. The final CAD model represents the truss members as one part and uses separate cylindrical pins at the connections.
CAD MODEL LINK: 

[truss_file.prt.zip](https://github.com/user-attachments/files/31765403/truss_file.prt.zip)

## Part 1 Questions: 

For context I used Ai and I am going about this as a conversation:
My first prompt was: Is this Yeilding because the trapezoid is more likely to slowly bend than snap in half like a rectangle or cylinder? 

From this question, I learned that the expected failure mode is not necessarily determined by the overall shape of the truss. Instead, factors such as whether the member is in tension or compression, the material being used, the applied stress, and the geometry of the individual member all affect the likely failure mode. ChatGPT explained that because A500 structural steel is a ductile material, yielding is a reasonable failure mode to consider for a member loaded in tension. This helped me understand that I should focus on the loading and material properties rather than assuming the trapezoidal shape itself determines how the member will fail.

The material we used is brittle because aluminum is inherently less strong than hardened steel?

From this question, I learned that I didn't completely understand the difference between brittleness and ductility. Now that AI helped me make the connection, I realize that the A500 structural steel is ductile because it can take a significant amount of loading and deform before it folds or fractures. When comparing the stress in my members to the yield strength of the steel, I found that my design stays below the allowable stress, which means yielding should not occur under the expected loading.

One design modification I pitched to the AI to help reduce the likelihood of fracture would be to add another support member to form an “X” in the middle of the truss. This would give both sides additional support and create another path for the forces to travel through the truss. This type of cross-bracing can also be seen in real-world bridges, such as the Medway Bridge in Rochester, England, which uses cross-bracing as part of its truss structure.

## Part 2 Questions:

When looking at the pin, I first asked myself, "How would this pin actually fail?" Since the force is acting perpendicular to the pin and the connection is designed as a single-shear connection, the pin is most likely to fail through shear. Because the pin is made from hardened tool steel and the given failure property is its yield shear strength, the expected failure mode is shear yielding.

So then my next question was, if you're only getting 8.33 kN of force and the maximum is 170 ksi, is the CAD nowhere close to its "breaking point"? The AI explained that the 170 ksi is not a force; it is the yield shear stress of the material. When we account for the safety factor of 4, the actual allowable stress is 42.5 ksi, which made the 8.33 kN force more significant than I initially thought. I learned that although the pin still has some margin before reaching its allowable stress, it is not as far from the design limit as I initially assumed.

### CAD Model Download
[truss_file.prt.zip](https://github.com/user-attachments/files/31765403/truss_file.prt.zip)


My source is: American Institute of Steel Construction (AISC), Steel Construction Manual, 15th Edition.
https://www.aisc.org/aisc/publications/steel-construction-manual/15th-ed-steel-construction-manual/?utm_source=chatgpt.com 

AISC identifies shear yielding as a structural limit state and gives shear-yielding calculations based on the material yield strength and the area subjected to shear. To support my choice of shear yielding as the expected failure mode, I looked at AISC's guidance on steel connections. AISC identifies shear yielding as a possible limit state when a structural component is subjected to shear. Since my pin is loaded in single shear, I determined shear to be the most relevant failure mode to investigate. The pin has a given yield shear strength of 170 ksi, and I used this value with a safety factor of 4 to determine an allowable shear stress of 42.5 ksi. My calculated pin area was then based on keeping the shear stress below this allowable value.

The change I would propose is to make the pin longer so that it has more engagement with the surrounding members. My reasoning comes from real-life fasteners, where the amount of material surrounding and engaging a fastener can affect the strength and stability of the connection. However, I learned that simply making the pin longer does not directly increase its shear strength. Increasing the pin diameter would be a more direct way to increase its shear area and reduce the likelihood of shear failure.

## Communicate Engineering Lessons 

Throughout this process, I learned how to naturally progress from determining internal forces and other mathematical concepts to translating those results into an actual CAD design. I also learned how to take a design from the initial concept and develop it into a complete model from scratch. I challenged myself in this assignment by going with my initial design idea instead of immediately choosing what seemed like the simplest design. An upside-down trapezoid was the first geometry that came to mind because of the way the shape could distribute the members and support the applied loads, so I decided to analyze and develop that idea rather than abandoning it for a simpler option.

This project also showed me that my current CAD skills still have room for improvement, particularly when translating engineering calculations into physical geometry. Because of this, I plan to continue developing my CAD skills throughout the remainder of this class so I can become more efficient and confident when creating engineering designs.

I also learned that a successful analytical calculation does not automatically guarantee that the CAD model represents the same design. The difference between my hand-calculated mass and CAD-predicted mass showed me that I need to verify dimensions, units, material properties, and geometry when transferring calculations into a CAD model.
