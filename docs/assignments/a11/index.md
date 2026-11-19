# A11 – Motor Selection

## Motor Selection and Attachments: Morgan Gregory

To begin I calculated the maximum speed the motor will need to endure. The calculations are shown below.

<img width="310" height="78" alt="Screenshot 2026-11-17 160008" src="https://github.com/user-attachments/assets/bbcf2910-86df-457b-bca4-dd1549428f87" />

Then I used the torque from A10 which was 1.296 Nm to find a motor that works.

Motor Selected: RPX52 52mm Brushless DC Motor

<img width="810" height="465" alt="Screenshot 2026-11-17 160231" src="https://github.com/user-attachments/assets/f64278e1-daa4-4b5a-8304-453791de1fbe" />

The speed-torque curve is shown below.

<img width="557" height="297" alt="Screenshot 2026-11-17 160458" src="https://github.com/user-attachments/assets/4839cb5a-5047-43f4-a00c-a7d474abb388" />

To begin the bracket design I listed my knowns and unknowns below.

<img width="728" height="173" alt="Screenshot 2026-11-17 194214" src="https://github.com/user-attachments/assets/cf2fedc9-5d46-4fe5-abe2-a2e4a153177d" />

I then created a FBD for the shear stress analysis.

<img width="382" height="194" alt="Screenshot 2026-11-17 194320" src="https://github.com/user-attachments/assets/ca228d15-9ce0-47e6-9f38-e68bb327fdf4" />

Then I used the knowns to find the unknown value as shown below using the reaction force.

<img width="864" height="430" alt="Screenshot 2026-11-17 194400" src="https://github.com/user-attachments/assets/555694cc-79b8-4978-86d0-81d8f9a83764" />

The minimum thickness was .154 mm but I chose 5 mm for convenience.

I began the CAD model below with a sketch and extrusion.

<img width="915" height="606" alt="Screenshot 2026-11-17 193140" src="https://github.com/user-attachments/assets/c6fb6ae5-6cf6-4d6e-9fe1-d1ff3333673a" />

<img width="820" height="435" alt="Screenshot 2026-11-17 193151" src="https://github.com/user-attachments/assets/f659084d-c76c-43f2-a46e-ce8ddcd301cb" />

I then made the sketch and extrusion for the shaft hole.

<img width="686" height="497" alt="Screenshot 2026-11-17 193130" src="https://github.com/user-attachments/assets/07b47833-5fc8-455d-939e-4cc29c8839fa" />

Then I made the holes using a centerline and the hole wizard tool. The screw size is M4.

<img width="1917" height="843" alt="Screenshot 2026-11-17 193654" src="https://github.com/user-attachments/assets/1d8bf5e1-0784-4ee9-a140-cca25aac328c" />

<img width="864" height="588" alt="Screenshot 2026-11-17 193702" src="https://github.com/user-attachments/assets/007009ed-5d07-4651-b456-f8aba3a8b2b2" />

Then I did the same on the other side using the diameters from the drawing of the motor.

<img width="989" height="686" alt="Screenshot 2026-11-17 194031" src="https://github.com/user-attachments/assets/8976a27b-e6da-493e-9264-d4aeae314322" />

Final part shown below.

<img width="746" height="537" alt="Screenshot 2026-11-17 194059" src="https://github.com/user-attachments/assets/aa1cc5e7-4bf4-448b-af9a-f4f28c6095cc" />

[A11 Motor Bracket.zip](https://github.com/user-attachments/files/35001412/A11.Motor.Bracket.zip)

I then began the coupling design using the same process, knowns and unknowns, FBD, then equations. The torsion equation was used.

<img width="815" height="232" alt="Screenshot 2026-11-17 194825" src="https://github.com/user-attachments/assets/beddafdd-0f22-46d5-affc-9e7de9daaa75" />

<img width="613" height="678" alt="Screenshot 2026-11-17 194837" src="https://github.com/user-attachments/assets/f3b40e59-92cd-4cb1-909d-837243d3a3a7" />

## Analyze and design a Frame (Lexie Cox)

In order to have a stable frame it needs to have connectors. To find which bracket I needed to choose I needed to find the torsion created by the motors. First I listed my knowns and unknowns. The 300 mm of length is from the previous assignment. 


<img width="455" height="177" alt="Screenshot 2026-11-19 034954" src="https://github.com/user-attachments/assets/454387c9-a3e0-4a28-8b51-ab69587fa26e" />


Then I created a Free body diagram showing how the motors will twist the screws. 

<img width="212" height="241" alt="Screenshot 2026-11-19 034957" src="https://github.com/user-attachments/assets/a88cd2ef-9f1b-4c43-9e79-e09b0f1e0335" />


I then found the torsion by finding the moments of the reacting forces of points A and B.

<img width="497" height="500" alt="Screenshot 2026-11-19 035003" src="https://github.com/user-attachments/assets/d6f6a435-b62a-48ee-bbfc-7baddcca0ba0" />


After finding the torsion that the motors would cause I needed to find a bracket that will support the frame through this force. I chose this triangle bracket: https://www.mcmaster.com/4844N44/?utm_term=t-slotted+framing+mounting+brackets&matchtype=e&campaignid=22726943438&adgroupid=181516498693&location=9191972&gad_source=1&gad_campaignid=22726943438&gbraid=0AAAAACLR9bxoQx36KLF0mBsANRs9y9QD6&gclid=CjwKCAjwnZfPBhAGEiwAzg-VzLbTAmYf7XUBDFs7MAYUOkFyr6vDTXVNg8zAIX-icwUoSbluXYTjeRoCbBsQAvD_BwE 

I chose this bracket because I know that triangles make better supports and are overall stronger than a regular L-shaped bracket. I also found that it was the correct dimensions for the frame I was about to create. 

In the assembly I started out by putting just the assembly from assignment 10 as a good starting point. 

<img width="197" height="470" alt="Screenshot 2026-11-19 030939" src="https://github.com/user-attachments/assets/3a93a55a-5353-40f6-a199-8e3fb08cb1ff" />

I then found the part and material that would make up the actual frame of the assembly. I had to make cuts in the piece to accommodate for the size of the crosshead. Each cut piece is below:

Top:

<img width="1197" height="502" alt="Screenshot 2026-11-19 031224" src="https://github.com/user-attachments/assets/52925ae0-da96-4cc4-b4a4-41deef6ea1ce" />

Sides:

<img width="876" height="333" alt="Screenshot 2026-11-19 031202" src="https://github.com/user-attachments/assets/b58902ec-b8a0-4aa5-b20b-68230b321a0a" />

Bottom:

<img width="1197" height="502" alt="Screenshot 2026-11-19 031224" src="https://github.com/user-attachments/assets/065b981d-3c81-4dd8-b9b3-ba96e9affaf7" />

I then put the frame together and merged the two parts. 

<img width="280" height="420" alt="Screenshot 2026-11-19 030954" src="https://github.com/user-attachments/assets/7c1f7977-e7d7-4872-be04-dfdeaefb1844" />

Then I found the CAD model of the bracket I chose and put it on the top of the frame. I ended up having to take the brackets off because when I went to do the FEA it would not work. 

<img width="627" height="713" alt="Screenshot 2026-11-19 031114" src="https://github.com/user-attachments/assets/12a90070-b02f-4268-82f3-4fe13691b327" />

<img width="746" height="693" alt="Screenshot 2026-11-18 232906" src="https://github.com/user-attachments/assets/bf412073-360a-40d8-b7df-83a15f00f24d" />

[Assignment11.zip](https://github.com/user-attachments/files/35074245/Assignment11.zip)

After creating the assembly I had to change the assembly to a part in order to do the FEA diagrams. For this I made the mesh pretty fine in order for the simulation to work. 

<img width="573" height="391" alt="Screenshot 2026-11-19 022701" src="https://github.com/user-attachments/assets/0cddf9f6-e125-42c5-af98-1897defa852b" />

<img width="562" height="430" alt="Screenshot 2026-11-19 022710" src="https://github.com/user-attachments/assets/8c394d27-3027-4278-b1c2-fb2e2967cf10" />

The maximum von Mises stress was around 1.573 MPA and this occurred in the middle of the top frame. The maximum vertical deflection was around 0.025 mm which also occurred in the middle of the top frame. The factor of safety it gave me was 32.546. The main thing that I would say would improve this deflection would be if the brackets were able to be used in the FEA diagrams.

For the next set of FEA diagrams the forces will be coming from the sides. I also meshed these components pretty fine. 

<img width="576" height="437" alt="Screenshot 2026-11-19 022717" src="https://github.com/user-attachments/assets/580342e9-1f86-453c-a0a5-6b57df10538d" />

<img width="572" height="471" alt="Screenshot 2026-11-19 022729" src="https://github.com/user-attachments/assets/04876e31-bfea-4ecc-b433-959eaa2eebcd" />

The maximum von Mises stress was around 0.8941 Mpa. This occurred at the bottom of the frame below the bottom frame. The maximum vertical deflection was around 0.004457 mm. This occurred in the middle of the side frames and they bent in. The factor of safety was 142.6. This is a very optimal factor of safety. One thing that I would change about this design is maybe making the screws shorter if possible making the entire thing smaller. This would make it more secure and have less of an ability to bend. 

## Design Floating Bearing Mount: ( Ethan Cornett)

<img width="3024" height="4032" alt="IMG_2037" src="https://github.com/user-attachments/assets/281ede0e-0c33-47c3-88f3-f2dd81ab00f9" />

<img width="672" height="666" alt="Screenshot 2026-11-18 221836" src="https://github.com/user-attachments/assets/e6ba0534-de16-4578-b30c-957d6881cfb8" />

<img width="1390" height="838" alt="Screenshot 2026-11-17 154155" src="https://github.com/user-attachments/assets/fd42b500-430c-48fa-bd3a-bfe6736fb2ef" />

CAD in more depth:

<img width="942" height="824" alt="image" src="https://github.com/user-attachments/assets/6cee662a-ccdb-4f9e-96e1-ebdf1a85f885" />

<img width="704" height="764" alt="image" src="https://github.com/user-attachments/assets/80526366-e6ac-4e8c-ab0a-0876a2a1f38e" />

<img width="796" height="818" alt="image" src="https://github.com/user-attachments/assets/08616bf0-c69b-4a4f-8d1d-b34b7ba76c8d" />

<img width="790" height="786" alt="image" src="https://github.com/user-attachments/assets/c1271f14-80cc-4e32-9c5e-02973a6bf190" />

<img width="954" height="904" alt="image" src="https://github.com/user-attachments/assets/54038b85-a491-4ce7-bb38-66e60cf9ff22" />

<img width="766" height="758" alt="image" src="https://github.com/user-attachments/assets/91ee8ab8-8313-4c66-a1cb-a49c5769cb2d" />

<img width="854" height="836" alt="image" src="https://github.com/user-attachments/assets/acaae8e5-08a6-4b5c-b2f0-1655cfbe82c1" />

Decided to make the base 2.5 x 2.5 x .75 so that the bracket is small enough to fit in smaller spaces and to save on material. The Tolerances I used was RC3 with a diameter between .4-.71 which ours is .5 
The tolerances were based on the above picture where I minus the given values by the starting diameter. 

## Bill of Materials and Labor Costs

| Item Number | Quantity | Name | Cost/Item | Cost | Purchase Link |
| ---: | ---: | --- | ---: | ---: | --- |
| 1 | 2 | Leadscrew | $56.52 | $113.04 | [Lead Screw](https://www.roton.com/product/acme-stainless-steel-screw-right-59837/) |
| 2 | 2 | Nut/Flange | $179 | $357.20 | [Nut](https://www.mcmaster.com/97790A110/) |
| 3 | 1 | Crosshead | $200 | $200.00 | N/A |
| 4 | 2 | Bearing Mount | $21.45 | $42.90 | N/A |
| 5 | 4 | Frame | $17.60 | $70.40 | N/A |
| | | | **Total Cost** | **$783.54** | |

| Person | Hours worked | Cost/hour | Cost |
| --- | ---: | ---: | ---: |
| Ethan Cornett | 10 | $30 | $300 |
| Morgan Gregory | 10 | $30 | $300 |
| Lexie Cox | 10 | $30 | $300 |
| | | **Total Cost** | **$900** |



Lessons Learned: ( Ethan Cornett)

1. How to choose a RC3 fit to fit a leadscrew-

I learned how to compare motor torque and rotational speed requirements to the mechanical requirements of a leadscrew. This helped me understand why both torque capacity and speed must be considered when selecting a motor for a tensile testing machine.

2. Coupler/Frame/motor mount/Bearing Design:
   
We learned how to apply torsional shear stress, bearing stress, and clearance fit calculations to design the coupler, motor mount, frame connections, and floating bearing mount. I also learned how proper alignment, material selection, and dimensional tolerances affect the strength, stability, and overall functionality of a mechanical assembly.

3. Frame Optimization: I learned how small geometric changes, such as adding fillets around mounting holes, can affect stress concentrations. I also learned that reducing stress does not always require increasing the overall size or mass of a component.

4. Bearing Mount and Tolerances: I learned how to apply RC3 fit classifications when designing a floating bearing mount. I also learned the importance of distinguishing between clearance holes for fasteners and functional tolerances for rotating components.

## References

https://electrocraft.com/products/bldc/rpx52/

## 2157 section: (Ethan Cornett)

All the drawings:

[a_11_bearing_2.drw.zip](https://github.com/user-attachments/files/35065244/a_11_bearing_2.drw.zip)

