# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure

Connect the supply (+5V) to the circuit Switch ON the main switch If the output is 1, then the led glows.




## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: S.M.Syed Mokthiyar
RegisterNumber: 212222230156
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: S.DEEPAK RAJ
RegisterNumber: 212222240023

1. Program to design a half subtractor:

module ex4(a,b,diff,borr);
input a,b;
output diff,borr;
assign diff=(a^b);
assign borr=((~a)&b);
endmodule 

2. Program to design a full subtractor:

module ex41(a,b,bin,diff,borr);
input a,b,bin;
output diff,borr;
assign diff=a^b^bin;
assign borr=((~a)&b)|(b&bin)|((~a)&bin);
endmodule 
```
## Truthtable
### Half Subtractor
![HS TT EXP4](https://github.com/syedmokthiyar/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118787294/7a7af21a-eab0-4ba2-9560-9d127eafdbdd)

### Full Subtractor
![FS EXP4 TT](https://github.com/syedmokthiyar/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118787294/8448d193-a839-4983-ad93-5e23f8d33659)


##  RTL realization:
### Half Subtractor
![HS EXP4 W](https://github.com/syedmokthiyar/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118787294/9cad8913-2c72-45cc-911a-c33f772a86ae)

### Full Subtractor
![FS EXP4 W](https://github.com/syedmokthiyar/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118787294/4a0d45ec-e677-42b7-89c4-6b67040060f9)

## Waveform:
### Half Subtractor
![HF EXP4 WV](https://github.com/syedmokthiyar/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118787294/e74ee74b-5c45-4cf7-b69f-b14e333e32e2)

### Full Subtractor
![FB EXP4 WF](https://github.com/syedmokthiyar/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118787294/48265ba3-51fc-4def-9432-ddbfc46ccd00)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
