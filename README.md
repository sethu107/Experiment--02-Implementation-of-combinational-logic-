# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D F2=xy’z+x’y’z+w’xy+wx’y+wxy

1.AND gate The AND gate is an electronic circuit that gives a high output (1) only if all its inputs are high. A dot (.) is used to show the AND operation i.e. A.B or can be written as AB Y= A.B

2.OR gate The OR gate is an electronic circuit that gives a high output (1) if one or more of its inputs are high. A plus (+) is used to show the OR operation. Y= A+B

## Logic Diagram
## Procedure
1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.
## Program:
```python
Developed by: K. Sethupathi
RegisterNumber: 212223040189
F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
module f1(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire p,q,r,s,t;
assign p = (~A & ~B & ~C & ~D);
assign q = (A & ~C & ~D);
assign r = (~B & C & ~D);
assign s = (~A & B & C & D);
assign t = (B & ~C & D);
assign F1 = p | q | r | s | t;
endmodule

F2=xy’z+x’y’z+w’xy+wx’y+wxy
module imp(w,x,y,z,F2);
input w,x,y,z;
output F2;
wire p,q,r,s,t;
assign p= (x & ~y & z);
assign q= (~x & ~y & z);
assign r= (~w & x & y);
assign s= (w & ~x & y);
assign t= (w & x & y);
assign F2= p | q | r | s | t;
endmodule
```
## Output:
## RTL realization
# F1:
![image](https://github.com/sethu107/Experiment--02-Implementation-of-combinational-logic-/assets/149347373/1a0359aa-aeac-43ab-adff-2d11bf26bd58)
# F2:
![image](https://github.com/sethu107/Experiment--02-Implementation-of-combinational-logic-/assets/149347373/ddd8ec79-2f7e-4347-94f2-fc59ef676b4d)
## Timing Diagram:
# F1:
![image](https://github.com/sethu107/Experiment--02-Implementation-of-combinational-logic-/assets/149347373/a12a693c-7912-4ce8-88d3-f3de3ca551e0)
# F2:
![image](https://github.com/sethu107/Experiment--02-Implementation-of-combinational-logic-/assets/149347373/784dab1c-277a-4f85-ba1a-a60b1184cf8b)


## RTL
## Timing Diagram
# F1:
![image](https://github.com/sethu107/Experiment--02-Implementation-of-combinational-logic-/assets/149347373/ab1d3038-1888-4f05-8dd8-ed3e7341642a)
# F2:
![image](https://github.com/sethu107/Experiment--02-Implementation-of-combinational-logic-/assets/149347373/c07fae56-4127-4bc8-bfd9-98a9cecfaaf1)


## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
