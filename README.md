## EXP2:BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 
```

  module exp2(a,b,c,d,w,x,y,z,f1,f2);
  input a,b,c,d,w,x,y,z;
  output f1,f2;
  wire x1,x2,x3,x4,x5,y1,y2,y3,y4,y5;
  assign x1=((~a)&(~b)&(~c)&(~d));
  assign x2=(a&(~c)&(~d));
  assign x3=((~b)&(c)&(~d));
  assign x4=((~a)&(b)&(c)&(d));
  assign x5=(b&(~c)&(d));
  assign f1=x1|x2|x3|x4|x5;
  
  assign y1=(x&(~y)&(z));
  assign y2=((~x)&(~y)&z);
  assign y3=((~w)&x&y);
  assign y4=(w&(~x)&(y));
  assign y5=(w&x&y);
  assign f2=y1|y2|y3|y4|y5;
  endmodule

```

**Developed by: Ameen Basha A**
**RegisterNumber: 212224220008**


**RTL realization**

**Output:**

**Truth Table**

i) F1 image

![image](https://github.com/user-attachments/assets/4a856c82-a5be-4657-b9e9-605ea0322d7f)

ii) F2 image

![image](https://github.com/user-attachments/assets/337078ef-2a86-47eb-8409-f5e042def9f9)

**RTL**


![image](https://github.com/user-attachments/assets/b22d9eb5-28c4-4975-b763-236b6f2e7d94)

**Timing Diagram**
![image](https://github.com/user-attachments/assets/45528523-01fb-4d9b-87f7-44123bbab851)
