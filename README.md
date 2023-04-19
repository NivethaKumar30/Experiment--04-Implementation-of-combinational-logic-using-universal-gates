# Experiment--04-Implementation-of-combinational-logic-using-universal-gates
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

Using NAND Operation:
```
module comb1(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R;
assign P = C&(~B)&(~A);
assign Q = D&(~C)&(~A);
assign R = (~C)&B&(~A);
assign F = (~P&~Q&~R);
endmodule
```
Using NOR Operation:
```
module comb2(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R,S;
assign P = C&(~B)&A;
assign Q = D&(~C)&A;
assign R = C&(~B)&A;
assign S = ~(P|Q|R);
assign F = ~S;
endmodule
```

## Output:

Using NAND Gate

RTL realization

![i1](https://user-images.githubusercontent.com/119559844/232985189-951ec343-a3f7-48eb-b9ee-9e1093af1b61.png)

Truth Table:

![i2](https://user-images.githubusercontent.com/119559844/232985200-44096dbd-7132-44b9-8332-18b9ae7b1f3f.png)

Timing Diagram

![i3](https://user-images.githubusercontent.com/119559844/232985213-2442ade5-e2af-46b4-a32f-cab16d1c7f5b.png)

Using NOR Gate

RTL realization

![i4](https://user-images.githubusercontent.com/119559844/232985233-7d346aa2-56a9-4ab4-ab83-7e241ac7b86d.png)

Truth Table:

![i5](https://user-images.githubusercontent.com/119559844/232985238-7d381321-80d7-4bf1-8554-73ae85238dfa.png)

Timing Diagram

![i6](https://user-images.githubusercontent.com/119559844/232985253-ebc58e54-1464-44f6-9bf5-296ec781a7aa.png)

## Result:

Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
