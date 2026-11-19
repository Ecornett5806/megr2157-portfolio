# A11 – Motor Selection

Purpose




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

Analyze and design a Frame

Chosen connecter:

https://www.mcmaster.com/4844N44/?utm_term=t-slotted+framing+mounting+brackets&matchtype=e&campaignid=22726943438&adgroupid=181516498693&location=9191972&gad_source=1&gad_campaignid=22726943438&gbraid=0AAAAACLR9bxoQx36KLF0mBsANRs9y9QD6&gclid=CjwKCAjwnZfPBhAGEiwAzg-VzLbTAmYf7XUBDFs7MAYUOkFyr6vDTXVNg8zAIX-icwUoSbluXYTjeRoCbBsQAvD_BwE 

This is chosen because it fits the 

Design Floating Bearing Mount

<img width="3024" height="4032" alt="IMG_2037" src="https://github.com/user-attachments/assets/281ede0e-0c33-47c3-88f3-f2dd81ab00f9" />

<img width="672" height="666" alt="Screenshot 2026-11-18 221836" src="https://github.com/user-attachments/assets/e6ba0534-de16-4578-b30c-957d6881cfb8" />

<img width="1390" height="838" alt="Screenshot 2026-11-17 154155" src="https://github.com/user-attachments/assets/fd42b500-430c-48fa-bd3a-bfe6736fb2ef" />



Decided to make the base 2.5 x 2.5 x .75 so that the bracket is small enough to fit in smaller spaces and to save on material. The Tolerances I used was RC3 with a diameter between .4-.71 which ours is .5 
The tolerances were based on the above picture where I minus the given values by the starting diameter. 



Bill of Materials and Labor Costs



Lessons Learned

1. How to choose a RC3 fit to fit a leadscrew-

I learned how to compare motor torque and rotational speed requirements to the mechanical requirements of a leadscrew. This helped me understand why both torque capacity and speed must be considered when selecting a motor for a tensile testing machine.

2. Coupler/Frame/motor mount/Bearing Design:
   
We learned how to apply torsional shear stress, bearing stress, and clearance fit calculations to design the coupler, motor mount, frame connections, and floating bearing mount. I also learned how proper alignment, material selection, and dimensional tolerances affect the strength, stability, and overall functionality of a mechanical assembly.

3. Frame Optimization: I learned how small geometric changes, such as adding fillets around mounting holes, can affect stress concentrations. I also learned that reducing stress does not always require increasing the overall size or mass of a component.

4. Bearing Mount and Tolerances: I learned how to apply RC3 fit classifications when designing a floating bearing mount. I also learned the importance of distinguishing between clearance holes for fasteners and functional tolerances for rotating components.

## References

https://electrocraft.com/products/bldc/rpx52/

2157 section: (Ethan Cornett)

All the drawings minus the Assembly are in here 
[a_11_bearing_2.drw.zip](https://github.com/user-attachments/files/35065244/a_11_bearing_2.drw.zip)

