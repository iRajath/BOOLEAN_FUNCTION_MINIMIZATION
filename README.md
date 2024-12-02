# BOOLEAN_FUNCTION_MINIMIZATION

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

Developed by: S Rajath RegisterNumber: 24900186*/

```
module exp2(A,B,C,D,W, X, Y, Z, F1, F2);
input A, B, C, D;
output F1;
wire x1, x2,x3,x4,x5;
assign x1=(~A) & (~B) & (C) & (~D);
assign x2=(~A) & (C) & (~D);
assign x3=(~B) & (C) & (~D);
assign x4= (~A) & (~B) & (C) & (~D);
assign x5=(~B) & (C) & (~D);
assign F1=x1|x2|x3|x4|x5;
input W,X,Y,Z;
output F2;
wire a1,a2, a3,a4,a5;
assign a1=(~W) & (~X) & (~Y) & (~Z);
assign a2=(~W) & (~Y) & (~Z);
assign a3=(~X) & (~Y) &(~Z);
assign a4=(~W) & (~X) & (~Y)&(~Z);
assign a5=(~X) & (~Y) & (~Z);
assign F2=a1|a2|a3|a4|a5;
endmodule
```

**RTL realization**

![image](https://github.com/user-attachments/assets/81defa7e-378a-40cc-a42d-5e3f517f938e)

**True Table**

![image](https://github.com/user-attachments/assets/4a3070bd-f3ab-4857-ac4a-37e87ba798f8)

![image](https://github.com/user-attachments/assets/bc31d0f4-f954-495e-81ac-5fdc222c8f39)


**RTL**

**Timing Diagram**

![image](https://github.com/user-attachments/assets/b9cd6b76-a682-4673-91c9-61f6b4a44af4)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

