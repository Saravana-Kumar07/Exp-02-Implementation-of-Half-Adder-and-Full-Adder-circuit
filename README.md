# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
## Aim:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

## Half Adder:
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

## Full Adder: 
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

### Figure -01 HALF ADDER: 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

### Figure -02 FULL ADDER:

## Procedure:

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:

## Half Adder:
```
module HalfAdder(A,B,sum,carry);
input A,B;
output sum,carry;
xor(sum,A,B);
and(carry,A,B);
endmodule
```
## Full Adder:
```
module FullAdder(a,b,c,Sum,Carry);
input a,b,c;
output Sum,Carry;
assign Sum = ((a^b)^c);
assign Carry = ((a&b) | (b&c) | (c&a));
endmodule
```
\*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: Saravana Kumar S

RegisterNumber: 212221230088
\*

## Output:
### Half Adder:
### RTL:
![](./hf.jpg)
### Timing Diagram:
![](./halfadder1.png)
### Truth Table: 
![](./TThalf.png)
### Full Adder:
### RTL:
![](./full_pic.jpg)
### Timing Diagram:
![](./fulladder1.png)
### Truth Table:
![](./TTfull.png)
## Result:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming is successfully done.
