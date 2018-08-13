
### Reflection

A manual parameter tunining approach has been used in this project, first I set the D and I parameters to zero, and tried different values for the 
P parameter.

A small value for the P parameter leads to weak steering response, which might lead the vehicle to get off track in areas where there is a sharp turn in the road, 
below is a recorded video showing the simulation with PID parameters set to

[(P=0.05, I=0.0, D=0.0)](./videos/P=0.05,I=0.0,D=0.0.mp4)

---

A large value for the P parameter leads to excessive wavering, due to the strong response to any small error 
which is shown in the below video, with PID parameters set to

[(P=0.4, I=0.0, D=0.0)](./videos/P=0.4,I=0.0,D=0.0.mp4)

---

So a 0.2 value for the P parameter was found to give reasonable results, the wavering couldn't be completely
eliminated though, without setting the D parameter, which was adjusted next, below is the simulation with
PID parameters set to

[(P=0.2, I=0.0, D=0.0)](./videos/P=0.2,I=0.0,D=0.0.mp4)

---

With P set to a reasonable value, we can move on to tuning the D parameter, the D parameter was gradually increased starting with 1.0,
until the wavering was almost eliminated at a value of 3.0, below is the simulation with PID parameters set to

[(P=0.2, I=0.0, D=3.0)](./videos/P=0.2,I=0.0,D=3.0.mp4)

---

Lastly the I parameter was set to a small value (0.0004), to eliminate any offset that the vehicle may develop over time, here we note that
I has to be a very small value, since it is multiplied by the error integrated over the whole period of the simulation, which might reach a high value,
below is the simulation with the parameters set to

[(P=0.2, I=0.0004, D=3.0)](./videos/P=0.2,I=0.0004,D=3.0.mp4)

---
