# A6 

## A6 Overview

For this assignment, I converted the bracket and link from the previous assignment into parametric CAD models. The important dimensions were replaced with user-defined parameters and Creo relations so that changes to the main design variables would automatically update the related geometry. I also used an analytical equation to connect the required area moment of inertia to the bracket cylinder diameter and applied different tolerances based on the function of each dimension.

The final models were tested by changing parameter values and regenerating the parts. The engineering drawings were then created from the final models and included third-angle projection, dimensions, general tolerances, and tighter tolerances on functional mating features.

### ZIP FIles for each Model and Drawings:

[a6_clip.drw.zip](https://github.com/user-attachments/files/32887722/a6_clip.drw.zip)

[a6_bracket_drawing.drw.zip](https://github.com/user-attachments/files/32887721/a6_bracket_drawing.drw.zip)

[a5_bracket_clip.prt.zip](https://github.com/user-attachments/files/32887719/a5_bracket_clip.prt.zip)

[a6.prt.zip](https://github.com/user-attachments/files/32887730/a6.prt.zip)


## Bracket Parametric Design

The bracket was originally modeled during the previous assignment using the results of the strength and stiffness analysis. For this assignment, I converted the important dimensions of the existing CAD model into user-defined parameters and relations. This allowed the geometry to be controlled by meaningful design variables instead of having each dimension entered independently.

The main parameters used for the bracket included A_LENGTH, B_LENGTH, PRACTICAL_LENGTH, TOP_WIDTH, BOTTOM_WIDTH, HEIGHT_T, CONNECTOR_WIDTH, and CYLINDER_DIAMETER. These parameters were selected because they control the major lengths, widths, thicknesses, and functional features of the bracket.

The parameters were connected to the model dimensions through Creo relations. For example, the major dimensions of the bracket were assigned directly to parameters such as A_LENGTH, B_LENGTH, and PRACTICAL_LENGTH. This allowed multiple features to respond to a single parameter instead of requiring each feature to be changed manually.

The following images show the parameters used for my bracket:

<img width="1084" height="274" alt="Screenshot 2026-09-30 235701" src="https://github.com/user-attachments/assets/97c51f3a-5619-4cca-86ee-5ea4923d35c4" />

<img width="1044" height="252" alt="Screenshot 2026-09-30 235650" src="https://github.com/user-attachments/assets/e27d9d98-7546-4a4e-8915-8dc25f5bac60" />

<img width="1038" height="266" alt="Screenshot 2026-09-30 235639" src="https://github.com/user-attachments/assets/1ec45378-2296-44ac-88b4-67221a47e364" />

The following images show the Creo relations used to control the bracket dimensions:

<img width="366" height="410" alt="Screenshot 2026-09-30 235927" src="https://github.com/user-attachments/assets/8abaed67-58e6-408a-8b34-828e354071c1" />

<img width="640" height="172" alt="Screenshot 2026-09-30 235938" src="https://github.com/user-attachments/assets/1fee1177-2879-4c1d-8e48-41ea8c90caac" />

I also tested the parametric behavior of the model by changing parameter values and regenerating the part. The associated dimensions updated automatically when the controlling parameter changed. This confirmed that the model was driven by the parameters and relations rather than only by manually entered dimensions.
The bracket also uses an analytical equation to relate the required area moment of inertia to the cylinder diameter. The purpose of this relation was to determine the cylinder diameter from the required moment of inertia. Rather than calculating a value separately and manually entering the result into the CAD model, the relationship was entered directly into Creo. This allowed the cylinder diameter to respond automatically if the required moment of inertia changed.

## Bracket model step by step:

<img width="744" height="488" alt="Screenshot 2026-10-01 003413" src="https://github.com/user-attachments/assets/4e6628b7-a9ae-4d2c-8540-bc1fc6b4eab6" />

<img width="742" height="466" alt="Screenshot 2026-10-01 003427" src="https://github.com/user-attachments/assets/9b4382aa-5b39-49aa-b035-258fd678bad4" />

<img width="728" height="554" alt="Screenshot 2026-10-01 003503" src="https://github.com/user-attachments/assets/b97ab1b7-5fd5-4778-9972-c46003bc5fe1" />

<img width="958" height="684" alt="Screenshot 2026-10-01 003524" src="https://github.com/user-attachments/assets/c325b236-41d5-47b9-869c-23ecf3ea2c1f" />

<img width="622" height="398" alt="Screenshot 2026-10-01 003535" src="https://github.com/user-attachments/assets/585a4a66-c052-49c4-8acc-b91cdaad7920" />

<img width="702" height="636" alt="Screenshot 2026-10-01 003603" src="https://github.com/user-attachments/assets/f103dd6e-1840-4a24-9d23-927fa63a1562" />

<img width="550" height="360" alt="Screenshot 2026-10-01 003615" src="https://github.com/user-attachments/assets/f07cfa65-c8f2-4c1b-aaf4-41701a475820" />

<img width="648" height="666" alt="Screenshot 2026-10-01 003633" src="https://github.com/user-attachments/assets/65f0af29-6dbd-461a-ae11-0065be9679bf" />


### Bracket CAD model Final Part 

<img width="898" height="954" alt="image" src="https://github.com/user-attachments/assets/e9f7f51e-9645-49bb-b5b4-d020e4ca2886" />

## Engineering Drawing

### Bracket Drawing

The bracket drawing was created as a multi-view engineering drawing using the final parametric CAD model. The drawing includes the necessary dimensions to describe the overall geometry, cylindrical feature, connecting section, and T-shaped sliding interface. The views were arranged using third-angle projection. The dimensions were placed in the views where the corresponding features could be shown without relying on measurements from the model itself.

<img width="1254" height="946" alt="Screenshot 2026-10-01 000539" src="https://github.com/user-attachments/assets/45748427-3ed8-4421-8c34-f2db52a53f9b" />

Specific tolerances were also applied to functional dimensions where the fit between the bracket and rigid T-beam required more control. These dimensions were given individual tolerances rather than relying only on the general tolerance block. The sliding interface was treated as a functional feature because the bracket must slide over the rigid T-beam while still maintaining the intended fit. The gap dimensions were therefore controlled separately from non-critical dimensions.

## Link Parametric Design

### Link/Clip Design

The link used for this assignment was based on the clip designed during the previous assignment. Instead of remodeling the part, I used the existing CAD model and modified it to meet the requirements of the current assignment. The important dimensions of the clip were converted into user-defined parameters. These parameters control the overall size of the part as well as the features that allow the link to connect to the bracket.

Parameters for Clip:

<img width="1032" height="66" alt="Screenshot 2026-10-01 001739" src="https://github.com/user-attachments/assets/d733593f-17bc-49d3-8e6e-4048da318f93" />

<img width="1064" height="254" alt="Screenshot 2026-10-01 001732" src="https://github.com/user-attachments/assets/de509b83-e13a-4102-a8cf-8b695c566209" />

### Relations for Clip

<img width="1066" height="278" alt="image" src="https://github.com/user-attachments/assets/81dd59b1-d7ff-43ad-a37a-f2f24ff9c42f" />


## Process Clip CAD:

<img width="438" height="940" alt="Screenshot 2026-10-01 003938" src="https://github.com/user-attachments/assets/aad58700-ffd5-4f0c-903d-3ce3c937798f" />

<img width="476" height="926" alt="Screenshot 2026-10-01 003950" src="https://github.com/user-attachments/assets/cad77995-e37d-46b9-9fb4-c89f98ac0395" />

<img width="660" height="982" alt="Screenshot 2026-10-01 004016" src="https://github.com/user-attachments/assets/b461d6de-cd82-4831-af24-271441c8b71e" />

<img width="680" height="958" alt="Screenshot 2026-10-01 004032" src="https://github.com/user-attachments/assets/373842a7-eef5-452f-ad3e-12f28a5c2b99" />




### Final Design Clip

<img width="620" height="984" alt="image" src="https://github.com/user-attachments/assets/91a081a3-4971-4506-8986-b402116a3702" />

## Link Engineering Drawing

The link drawing was created using multiple views with a third-angle projection layout. The drawing includes dimensions for the overall geometry as well as the features required for assembly with the bracket.

<img width="1224" height="904" alt="image" src="https://github.com/user-attachments/assets/a1fdf6f2-dbb4-4f0c-a371-678d443362e1" />

The standard course tolerance block was included on the drawing:
Additional tolerance callouts were applied to critical features of the link. These tighter tolerances were used on mating features where dimensional variation could affect assembly with the bracket. Less critical dimensions were allowed to use the general tolerance values.
note was also included to identify the interface between the link and bracket.

## Reflections

### Engineering Lessons Learned

One of the main lessons from this assignment was that a CAD model becomes more useful when important dimensions are connected to design intent. Entering dimensions individually can produce the required geometry, but it makes the model harder to modify. Using parameters and relations allowed multiple features to respond to a smaller number of controlling dimensions.

I also learned that tolerancing is directly related to how a part functions. A mating surface requires more dimensional control than a feature that does not affect assembly. Applying a tighter tolerance to every dimension would increase manufacturing difficulty and potentially increase cost without providing a functional benefit. The tolerance therefore needs to match the purpose of the feature.

The drawing also demonstrated the importance of communicating design intent. A CAD model can show the shape of a part, but the engineering drawing communicates how the part should be fabricated and assembled. Dimensions, tolerances, and interface notes provide information that cannot be fully understood from the geometry alone.

Another lesson was the importance of part-to-part compatibility. The link and bracket cannot be designed independently because the dimensions of one part affect how the two parts assemble. Connecting the appropriate parameters between the parts helped maintain the intended interface.

## Analytical Equation

The analytical equation used to drive a dimension in the bracket was the area moment of inertia equation for a circular cross section:

<img width="232" height="110" alt="Screenshot 2026-10-01 004636" src="https://github.com/user-attachments/assets/2e82af6a-fac9-4be5-aa8b-fd3957c0b679" />

This equation was used to determine the cylinder diameter of the bracket based on the required area moment of inertia from the previous analysis.

The relationship was entered directly into Creo using relations rather than calculating the diameter separately and typing the final value into the model. The relation connected the required moment of inertia to the CYLINDER_DIAMETER parameter. When the value driving the relation changed, the calculated diameter updated during regeneration and the associated cylindrical geometry updated with it.

## Tolerance Selection

One tighter tolerance was applied to the 0.20 in dimension using ±0.01 in tolerance. This dimension is associated with the functional sliding interface of the bracket

A looser tolerance was applied to the 0.30 in dimension using ±0.02 in tolerance. This dimension controls a non-critical portion of the bracket

Using the tightest tolerance on every dimension would make manufacturing more difficult and could increase manufacturing and inspection costs. A tighter tolerance requires more precise processes and greater inspection control, so it should be reserved for dimensions where the function of the part requires that level of accuracy.

## Time Spent

I spent approximately 7 hours completing the assignment.
