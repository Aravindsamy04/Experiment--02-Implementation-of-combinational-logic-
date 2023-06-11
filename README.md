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
 
 ## Using NAND gates:
 
 NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Using NOR Gates:

Using NOR gates NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram
## Procedure:

1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.
## Program:
```
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: ARAVIND SAMY.P
RegisterNumber:  212222230011

F1:
module ff(a,b,c,d,f1);

input a,b,c,d;

output f1;

assign f1 = (~b&~d) | (~a&b&d) | (a&b&~c);

endmodule


F2:

module de (w,x,y,z,f2);

input w,x,y,z;

output f2;

assign f2 = (x&y)|(w&y)|(~y&z);

endmodule 
*/

```

## Output:

## RTL:
F1:

![RTL F1](https://github.com/Aravindsamy04/Experiment--02-Implementation-of-combinational-logic-/assets/113497037/63d2dd48-ce27-492d-971b-9200e3c46ecb)
F2:

![RTL F2](https://github.com/Aravindsamy04/Experiment--02-Implementation-of-combinational-logic-/assets/113497037/e1a102b4-1d93-4622-8bc9-c4d3b03444d1)

## Timing Diagram:
F1:
![TIMING F1](https://github.com/Aravindsamy04/Experiment--02-Implementation-of-combinational-logic-/assets/113497037/b0691d85-8e76-4532-8758-515bbacaf554)
F2:

![TIMING F2](https://github.com/Aravindsamy04/Experiment--02-Implementation-of-combinational-logic-/assets/113497037/39929ca6-119d-4104-9a9b-8b01e740427e)

## TRUTH TABLE :

![TRUTH TABLS](https://github.com/Aravindsamy04/Experiment--02-Implementation-of-combinational-logic-/assets/113497037/276b749d-7f4c-4e5a-9208-13c3f7eb94a6)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
