# A10 – Lead Screw Translating System

## Project Objective

The objective of this project was to conceptually design a mechanically driven tensile testing machine capable of applying up to 2 kN of axial tensile force to a test specimen. The system uses a leadscrew-driven crosshead to provide controlled, repeatable movement at speeds ranging from 1 to 50 mm/min. The design focuses on maintaining structural strength, minimizing crosshead deflection and misalignment, and providing reliable specimen gripping. Additional design considerations include selecting appropriate leadscrews, ensuring a factor of safety of 4, and developing a compact, safe, and ergonomic bench-top system. The final design must operate entirely through mechanical components, without electronics or software.

## Lead Screw: (Ethan Cornett)

1. Minimum Leadscrew Diameter

The first step in selecting the leadscrews was determining the minimum diameter required to safely support the tensile tester's maximum load of 2 kN. Since the design uses two identical leadscrews, the total load is distributed equally between them, resulting in an axial load of 1 kN per screw.

304 stainless steel was initially selected as the material for the leadscrews, with a yield strength of 205 MPa. A factor of safety of 4 was applied to determine the minimum required diameter.

The diameter was calculated using the axial stress relationship: O=F/A

The allowable stress was determined using the material yield strength and required factor of safety. The resulting theoretical minimum diameter was approximately 4.99 mm. I decided to use a diameter of 12.7mm or 1/2 inch. 

This calculation established the minimum structural requirement before selecting a commercially available leadscrew.

<img width="4284" height="5712" alt="IMG_1994" src="https://github.com/user-attachments/assets/79b9d623-2dfb-4c2f-89f1-5216699750c0" />

2. Rotational Speed Range

After establishing the minimum diameter, the next step was determining the rotational speed required to achieve the specified crosshead speed.

The tensile tester must operate between 1 mm/min and 50 mm/min. The relationship between linear crosshead speed and leadscrew rotational speed is:

V=nL

Where:

(V) = Linear crosshead speed (mm/min)

(n) = Leadscrew rotational speed (RPM)

(L) = Leadscrew lead (mm/rev)

The selected 1/2-10 Acme leadscrew has a lead of 0.100 inches per revolution, equivalent to 2.54 mm/rev, assuming a single-start thread.

Using this lead, the required rotational speed range is:

Minimum speed: 0.394 RPM

Maximum speed: 19.69 RPM

Both leadscrews will rotate at the same speed to maintain synchronized crosshead movement.

<img width="4284" height="5712" alt="IMG_1995" src="https://github.com/user-attachments/assets/9d68d5f8-824b-4c5c-bd6a-8606b45c5a86" />

3. Maximum Leadscrew Torque

The next calculation determined the torque required to drive both leadscrews while maintaining the required 2 kN tensile load.

Because the system uses two leadscrews, each screw carries approximately 1 kN of the applied load. The torque calculation accounts for the screw lead and the torque coefficient used in the preliminary design.

The calculated torque requirement was approximately:

T_i = FL/2pi(n)

T_T = 2FL/2pi(n)

T_S =FR_T(2)(N)

Torque per leadscrew: 11.47 in·lbf

Combined torque: 22.94 in·lbf (2.59 N·m)

A factor of safety of 4 was then applied to determine the design torque requirement.

The resulting combined design torque was approximately 10.36 N·m.

This value provides the preliminary torque requirement for selecting the mechanical drive system. Actual operating torque will also depend on the selected nut, lubrication, alignment, and friction.

4. Commercial Leadscrew Selection

After determining the minimum diameter, rotational speed range, and torque requirements, the team moved toward selecting a commercially available leadscrew.

The selected design uses two identical Roton 1/2-10 Acme leadscrews. The 1/2-inch nominal diameter exceeds the calculated minimum diameter of approximately 4.99 mm, while the 0.100-inch lead provides the required crosshead speed range at approximately 0.394–19.69 RPM.

Using identical leadscrews also allows both sides of the crosshead to move together, helping maintain alignment during tensile testing.

Supporting images:

<img width="1900" height="168" alt="image" src="https://github.com/user-attachments/assets/a942e818-a7cf-4b56-96bc-ac5d5b328644" />

Design Outcome:

The calculations established the initial requirements for the tensile tester's leadscrew system. The team determined the minimum required screw diameter, the rotational speed range needed to achieve the specified crosshead speeds, and the preliminary torque requirement for the drive system.

These calculations provided the foundation for selecting the commercial leadscrews and developing the remaining mechanical design.
Supporting images:

<img width="882" height="1166" alt="image" src="https://github.com/user-attachments/assets/e33f2c2e-001a-4fc4-b7aa-2ddf71d9b302" />

## Nut and Flange (Lexie Cox)

For the Nut and Flange I started out by listing all of the knowns and unknowns needed for the calculations.

<img width="697" height="345" alt="image" src="https://github.com/user-attachments/assets/163dc4e8-b955-4d80-95a5-cd1f75cf9a25" />

I then found the bending stress that would be on the chosen nut.

<img width="700" height="222" alt="image" src="https://github.com/user-attachments/assets/73c75ebf-1f4a-484f-82eb-429757df50b6" />

It is important to make sure that this is the correct chosen nut and that it would not fail in the machine. To do this I found the maximum bending stress. The calculated bending stress was less than the maximum bending stress meaning that this is the correct nut.

<img width="748" height="310" alt="image" src="https://github.com/user-attachments/assets/024c44ab-22c1-4258-80cd-dfe2fc2c52bb" />

## Crosshead + Assembly (Morgan Gregory)

Designing the Crosshead: Morgan Gregory
To begin, I needed to find both the length, from research, and the base, from the nut flange. The length was chosen to be 300 mm and the base was chosen from the flange nut diameter to be 31.75 mm. The rest of the knowns and unknowns are shown below.

<img width="455" height="330" alt="image" src="https://github.com/user-attachments/assets/affecb33-bd4d-495b-88d7-5d79ea54f774" />

I then found the maximum shear and yield stresses using the safety factor of 4.

<img width="394" height="189" alt="image" src="https://github.com/user-attachments/assets/ad332f8c-b85c-43c0-af11-6b56cccf9642" />

Now it is important to calculate minimum values such as thickness of the beam. I began by doing the stress analysis. I analyzed shear stress first and bending stress second. The math is shown below, with minimum h values. 6061 aluminum was the chosen material for its lighter weight and cost effectiveness.

<img width="850" height="290" alt="image" src="https://github.com/user-attachments/assets/91fb4e90-9a9d-486b-8968-abe6377aa40b" />

The minimum value of h for came from the bending stress so far at 11.33 mm.

Now it was important to find the h with the max deflection of .1 mm.

<img width="818" height="217" alt="image" src="https://github.com/user-attachments/assets/69f41f7a-5b58-4519-ae4a-055d9a017e5b" />

The deflection gave the final value of h as 21.3 mm.

Next is the drawing for the crosshead. Sketches are shown below. Holes are measured as 1 inch.

<img width="815" height="560" alt="image" src="https://github.com/user-attachments/assets/03f1a3b3-7e4f-4407-8260-a6f860a1f382" />

## Parametric Modeling - Morgan Gregory

I began by parametrically designing the crosshead in SolidWorks as shown below.

<img width="921" height="80" alt="image" src="https://github.com/user-attachments/assets/ab815211-cd49-4fa7-b102-59fcbceadf5b" />

<img width="1286" height="485" alt="image" src="https://github.com/user-attachments/assets/f810fa4c-db25-46b7-8840-884ac4db123d" />

<img width="1916" height="840" alt="image" src="https://github.com/user-attachments/assets/dc14b5f8-606c-4c22-bf80-6cc5d6924a63" />

<img width="1004" height="401" alt="image" src="https://github.com/user-attachments/assets/7dd0f926-0e76-409e-91ee-aeddceaf0ab1" />

<img width="1004" height="401" alt="image" src="https://github.com/user-attachments/assets/09cedc8a-174c-49c5-a11d-b4ae47a5c934" />

<img width="877" height="379" alt="image" src="https://github.com/user-attachments/assets/f817b956-bf1a-49dc-b6e2-428a55a6b362" />

Assembly: 

The SolidWorks Assembly is shown below and the part file for the crosshead and the assembly are below.

<img width="987" height="532" alt="image" src="https://github.com/user-attachments/assets/1c019b66-de2f-4694-885b-876c3dc9df6b" />

<img width="792" height="636" alt="image" src="https://github.com/user-attachments/assets/025aa102-b779-4363-9ff4-7e9d8a8049d4" />

<img width="721" height="625" alt="image" src="https://github.com/user-attachments/assets/a6a7e610-4010-45a9-b65a-461b0704f5d8" />

https://github.com/user-attachments/files/34723579/Crosshead.zip

https://github.com/user-attachments/files/34723581/A10Assembly.zip

## Lessons Learned (Lexie Cox)
In this assignment, we designed a conceptual tensile tester by establishing minimum testing requirements and calculating the specifications for its individual components. The most challenging aspect of the project was selecting appropriate bolt lengths and sourcing bearing fixtures that fit within our design constraints. This highlighted the critical importance of balancing cost, material properties, and applied forces when selecting off-the-shelf components for a mechanical design.

This assignment took us roughly 6 hours to complete.

## Cost (Lexie, Ethan, Morgan)

| Item Number | Quantity | Name | Cost/Item | Total Cost | Purchase Link |
|---|---:|---|---:|---:|---|
| 1 | 2 | Leadscrew | $56.52 | $113.04 | [Roton 59837](https://www.roton.com/) |
| 2 | 2 | Nut/Flange | $178.60 | $357.20 | [McMaster-Carr 97790A110](https://www.mcmaster.com/97790A110/) |
| | | **Grand Total** | | **$470.24** | |
## Lessons Learned (Lexie Cox)

## 2157 (Ethan Cornett)
First I fixed the two sides:

<img width="1768" height="1154" alt="image" src="https://github.com/user-attachments/assets/5c8f3135-647d-4fc6-95f0-1fa839d7df71" />

Then I added the force In the middle of the Beam at a 2KN amount:

<img width="1838" height="1112" alt="image" src="https://github.com/user-attachments/assets/fc933f1c-1a70-4730-ab9b-212fe3664c63" />

Defelction graph Fine Mesh pre changes:

<img width="980" height="856" alt="Screenshot 2026-11-11 131545" src="https://github.com/user-attachments/assets/4623bacf-d6ea-47ec-a804-c3b48d4bcb18" />

Von Mises Stress Graph Fine mesh pre-Changes: 

<img width="1104" height="940" alt="Screenshot 2026-11-11 131528" src="https://github.com/user-attachments/assets/5a8f2643-c61b-40f7-962e-8e51bed904e2" />

The safety factor I got was about 27.6 we got this from morgans value of 276 then we divided by the max stress value of the graph being 10 MPA. 

Now I moved on to a Middle between fine and course mesh: 

Von Mises Stress Graph Middle mesh pre-Changes

<img width="948" height="890" alt="Screenshot 2026-11-11 193225" src="https://github.com/user-attachments/assets/2a7a5b62-d5e0-4a4f-9604-dffccb6129bf" />

Defelction graph Middle Mesh pre changes:

<img width="680" height="828" alt="Screenshot 2026-11-11 193307" src="https://github.com/user-attachments/assets/87b06a2a-8669-418a-8cbd-aba495a97239" />

The safety factor I got was about 9 we got this from morgans value of 276 then we divided by the max stress value of the graph being 31.016 MPA.
Meaning even with the more course mesh we still are way above the 4-safety factor. 

Finally I used a super course mesh and the results were the following: 

Von Mises Stress Graph Course mesh pre-Changes

<img width="982" height="822" alt="Screenshot 2026-11-11 193357" src="https://github.com/user-attachments/assets/c5c9903a-dd62-49fe-b633-35522bae25e9" />

Defelction graph Course Mesh pre changes:

<img width="914" height="810" alt="Screenshot 2026-11-11 193407" src="https://github.com/user-attachments/assets/15f74e4f-02f8-4b24-8d01-e996c283dd55" />

The safety factor I got was about 9.25 we got this from morgans value of 276 then we divided by the max stress value of the graph being 29.828 MPA.
Meaning even with the super course mesh we still are way above the 4-safety factor. 

Optimization Pass:

For the optimization I decided to just add a small 2mm fillet to the holes to keep them rounded which should lead to slightly less stress around the holes. 
Von Mises Stress Graph Course mesh pre-Changes

Von Mises Stress Graph Course mesh post-Changes

<img width="1080" height="856" alt="Screenshot 2026-11-11 195022" src="https://github.com/user-attachments/assets/b4f19684-d6ad-4d71-8f99-c0dc3fc41e1c" />

Defelction graph Course Mesh post changes:

<img width="916" height="814" alt="image" src="https://github.com/user-attachments/assets/48f30510-d838-4f6f-b605-f45c09c52a47" />

The safety factor I got was about 9 we got this from morgans value of 276 then we divided by the max stress value of the graph being 30.667 MPA.

Von Mises Stress Graph Middle mesh post-Changes

<img width="968" height="828" alt="image" src="https://github.com/user-attachments/assets/88aec988-e4c8-4b5f-b485-7e0fac3c138d" />

Defelction graph Middle Mesh post changes:

<img width="900" height="798" alt="image" src="https://github.com/user-attachments/assets/06eae879-29a5-4ca4-9e17-3daa123519da" />

The safety factor I got was about 9 we got this from morgans value of 276 then we divided by the max stress value of the graph being 30.767 MPA.

Von Mises Stress Graph Fine mesh post-Changes

<img width="1020" height="846" alt="image" src="https://github.com/user-attachments/assets/143de777-7972-4c5f-aa59-f8f88479697c" />

Defelction graph Fine Mesh post changes:

<img width="900" height="804" alt="image" src="https://github.com/user-attachments/assets/457ea2f4-916b-49e9-ad7e-ffb01750b762" />

The safety factor I got was about 8.87 we got this from morgans value of 276 then we divided by the max stress value of the graph being 31.116 MPA.

## Drawing: 

[Crosshead.zip](https://github.com/user-attachments/files/34721985/Crosshead.zip)


## Refrences:

https://mechanicalc.com/reference/beam-deflection-tables

https://repositum.tuwien.at/bitstream/20.500.12708/200949/1/Demmel%20Stella%20-%202024%20-%20Design%20manufacturing%20and%20testing%20of%20an%20open-source...pdf
