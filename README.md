# Experiment--02-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
 
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

## Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram

Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram
## Procedure
## Program:
```
Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
Developed by: NIVETHA K
RegisterNumber: 212222230102
```

```
module ff(a,b,c,d,f1);
input a,b,c,d;
output f1;
assign f1 = (~b&~d) | (~a&b&d) | (a&b&~c);
endmodule

module de (w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2 = (x&y)|(w&y)|(~y&z);
endmodule 
```
## Output:

Output:
RTL:
FOR F1:

![image](https://github.com/NivethaKumar30/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/119559844/f071d1a7-5015-4f6a-8d56-c416fe018274)


For F2:

![2](https://github.com/NivethaKumar30/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/119559844/b84a5cd8-0306-411a-a8d8-bf5a19175b3c)

Timing Diagram:

For F1:

![3](https://github.com/NivethaKumar30/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/119559844/8a0fcee4-f1f5-480d-8a5a-7d2e7d21ccdd)

For F2:

![4](https://github.com/NivethaKumar30/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/119559844/4c33dabb-8e35-471b-9950-aaa0d2b5738f)


## Result:

TThus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
