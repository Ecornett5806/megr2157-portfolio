# A5 – Bracket & Link Design:

## Project Overview

The goal of this project was to design a bracket capable of carrying a horizontal strap load while maintaining the required strength and stiffness. The bracket was divided into five features, A through E, so that the load could be traced through the structure. Each feature was analyzed for both bending strength and stiffness using a safety factor of 4 and a maximum allowable deflection of 0.005 in. After completing the bracket design, a separate linkage was designed to connect Feature A to a 1-inch diameter shaft.

## Design Requirements:

Applied load: 700 lbf

Safety factor: 4

Material	ASTM A36 steel

Yield strength: 36,000 psi

Elastic modulus: 29 × 10⁶ psi

Allowable stress: 9,000 psi

Maximum feature deflection: 0.005 in

Shear deflection	Neglected

I selected a 700-lbf design load because the assignment requires the applied force to be greater than 500 lbf and less than 800 lbf. The load was traced through the bracket by using the reaction forces from one feature as the applied forces for the following feature.

I broke the bracket into five features, A through E, so I could follow the load through the structure instead of treating the entire bracket as one complicated part. Feature A receives the 700-lbf strap load, and the reactions from each feature were carried into the next feature as applied loads. Due to the symmetry of the bracket, the load was divided into 350-lbf reactions on each side. I used A36 steel with a safety factor of 4 and checked every feature for both bending stress and deflection. The strength analysis determined the minimum section size needed to prevent yielding, while the stiffness analysis determined the minimum size needed to keep deflection below 0.005 in. I compared the two results for each feature and used the larger requirement when selecting the final dimensions. This gave me a calculated starting point for the CAD model rather than choosing the bracket dimensions by trial and error.

### Section A: 

Feature A was the first part of the load path and was sized based on the force transferred from the strap into the bracket. The strength analysis was used to determine the required size of the cylindrical feature while maintaining the required safety factor. The preliminary diameter obtained from the strength calculation was approximately 0.420 in. This dimension provides the required cross-sectional area for the applied load under the simplified beam model. The resulting feature was then used to determine the reaction forces transferred into Feature B.

<img width="2284" height="3712" alt="63F08D7F-D508-4E24-91E8-CCB80D16F3A1" src="https://github.com/user-attachments/assets/f3b8749d-3e7a-4af4-823e-44266f435ea6" />

### Section B: 

Feature B transfers the load from Feature A into the two sides of the bracket. Because the bracket is symmetric, the 700-lbf applied load was divided into two 350-lbf reactions. For the stiffness analysis, using a 0.75-in beam length, A36 steel, and a maximum allowable deflection of 0.005 in resulted in a required moment of inertia of approximately \(2.65\times10^{-5}\text{ in}^4\). For the circular section used in the preliminary model, this corresponded to a diameter of approximately 0.153 in. The strength and stiffness requirements were then compared to determine the final practical dimension used for the CAD model.

<img width="2284" height="3712" alt="IMG_1640" src="https://github.com/user-attachments/assets/c6063490-071d-47c2-9846-f10400abc378" />

### Section C: 

Feature C was analyzed using the 350-lbf reaction from the symmetric load path. Modeling C as a cantilever with a length of 0.75 in produced a maximum bending moment of 262.5 lb-in. With an allowable stress of 9,000 psi, the required section modulus was 0.0292 in³, which required a section height of approximately 0.592 in when a 0.50-in width was used. The stiffness analysis required only approximately 0.201 in of section height to keep the deflection below 0.005 in. Therefore, strength governed the design of Feature C, and a practical dimension of approximately 0.50 × 0.60 in was selected.

<img width="2284" height="3712" alt="DC290B55-8380-4045-8D38-908A1049334F" src="https://github.com/user-attachments/assets/4888d488-8e7f-46e4-858b-d4c5f1089ffc" />

### Section D:

Results: Feature D was analyzed using the load transferred from the previous feature and was modeled as a cantilever for the preliminary calculation. Using a 350-lbf load and a 0.75-in length resulted in a maximum bending moment of 262.5 lb-in. The strength calculation required a section modulus of approximately 0.0292 in³, resulting in a required height of approximately 0.592 in for a 0.50-in-wide rectangular section. The stiffness calculation required approximately 0.201 in of height. Since the strength requirement was larger than the stiffness requirement, stress governed the preliminary D dimension, leading to a selected section of approximately 0.50 × 0.60 in.

<img width="2284" height="3712" alt="3FF9E648-B1D7-4D22-B150-73FCB656C6DC" src="https://github.com/user-attachments/assets/104a9d18-f64e-4ceb-a2fe-db01793545d7" />

### Section E:

Feature E was the final feature in the simplified load path and was analyzed using the same 350-lbf side load and 0.75-in preliminary length. The simplified cantilever model produced a bending moment of 262.5 lb-in. The strength calculation required a section modulus of approximately 0.0292 in³, corresponding to a height of approximately 0.592 in for a 0.50-in width. The stiffness calculation required approximately 0.201 in to satisfy the 0.005-in deflection limit. Therefore, under the simplified model, strength governed Feature E, and a preliminary section of approximately 0.50 × 0.60 in was selected.

The analysis showed that the load decreases into individual symmetric load paths, with the 700-lbf applied load producing approximately 350 lbf on each side of the bracket. For Features C through E, the bending-strength requirement was larger than the stiffness requirement under the simplified beam assumptions. For example, Feature C required approximately 0.592 in of section height for strength compared with 0.201 in for stiffness. A practical 0.60-in height was therefore selected for these preliminary sections. These calculations provided the minimum structural dimensions used as the starting point for the CAD model.

<img width="2284" height="3712" alt="IMG_1643" src="https://github.com/user-attachments/assets/dc344e73-9531-449b-a81f-851280c75c35" />

## Multiview Sketches

For the stress-analysis sketch, I created a detailed multiview representation of the bracket showing the front, top, and side views of the features being analyzed. The sketch identifies the important dimensions, applied loads, support locations, and critical cross-sections used in the bending-stress calculations. I also included the simplified free-body/beam representation used to model the more complicated bracket geometry. This allowed the actual geometry to be connected directly to the assumptions used in the strength equations.

For the stiffness-analysis sketch, I created a second multiview drawing showing the same bracket geometry but focusing on the dimensions and loading used for the deflection calculations. The sketch shows how each feature was simplified into a beam model and where the applied and reaction forces act. The 0.005-in maximum deflection requirement was used when determining the minimum required dimensions. Keeping the stress and stiffness sketches separate made it easier to see that the same physical features were being evaluated for two different failure conditions.

<img width="2284" height="3712" alt="IMG_1644" src="https://github.com/user-attachments/assets/51f931f7-a265-4089-a3e9-33a7b82d784c" />

## CAD MODEL MATH: 

I used the results from the stress and stiffness calculations to build the CAD model. The calculated minimum dimensions were used as starting points, and practical dimensions were selected where necessary. For example, the C–E sections required approximately 0.592 in for strength but only 0.201 in for stiffness, so a 0.60-in section height was used. I then modeled the entire bracket as one solid using extrusions, cuts, holes, and symmetry rather than creating A–E as separate parts.

<img width="2284" height="3712" alt="IMG_1645" src="https://github.com/user-attachments/assets/5d4571ed-9a58-461b-b081-25be284e1530" />

## CAD MODEL: 

<img width="492" height="914" alt="image" src="https://github.com/user-attachments/assets/787ae8b4-2887-47bf-95a3-61f503d57ba9" />


