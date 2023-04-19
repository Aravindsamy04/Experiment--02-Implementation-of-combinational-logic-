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

USING NAND:
   module combo1(a,b,c,d,f);
   input a,b,c,d;
   output f;
   wire p,q,r;
   assign p=(~c & b & a);
   assign q=(~d & c & ~a);
   assign r=(c & ~b & a);
   assign f=(~(~p & ~q & ~r));
   endmodule

USING NOR:
   module combo2(a,b,c,d,f);
   input a,b,c,d;
   output f;
   wire p,q,r;
   assign p=( c & ~b & a);
   assign q=( d & ~c & a);
   assign r=( c & ~b & a);
   assign f=(~(~( p | q | r)));
   endmodule
*/
```

## Output:

## USING NAND GATE:
## RTL:


![de1](https://user-images.githubusercontent.com/113497037/233161534-5c784497-173a-4643-8d99-f0a9fc7c6878.png)

## Timing Diagram:


![de 2](https://user-images.githubusercontent.com/113497037/233164132-9d723e21-0b58-4e4a-87d0-5eec0b71a9c8.png)

## TRUTH TABLE:

![de 3](https://user-images.githubusercontent.com/113497037/233164420-f64fdd5f-53c1-47c5-b86c-4ffe11238600.png)

## USING NOR:

## RTL :

![de4](https://user-images.githubusercontent.com/113497037/233164748-6fdc5db3-dc0a-4607-8020-fe7c975feb46.png)


## Timing Diagram :

![de 5](https://user-images.githubusercontent.com/113497037/233164945-61ab1ab5-9020-447d-8356-48c00f6c91fb.png)

## TRUTH TABLE :

![de 6](https://user-images.githubusercontent.com/113497037/233165073-3da34936-98ea-4e3f-a87b-f087dc8bf34a.png)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
