# Experiment--04-Half-Subtractor-and-Full-subtractor
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



Write the detailed procedure here 


## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: ARHAM S
RegisterNumber: 212222110005

### Half subtractor:
module halfsub(a,b,Diff,Borrow);
input a,b;
output Diff,Borrow;
assign Diff = (a^b);
assign Borrow = (~a&b);
endmodule

### Full subtractor
module fullsub(A,B,Bin,diff,borrow);
input A,B,Bin;
output diff,borrow;
assign diff=(A^B^Bin);
assign borrow=((~A&B)|(~(A^B)&Bin));
endmodule

```
##  RTL realization:

## half subtractor:

![image](https://github.com/22009011/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343461/8b34cb8c-86f8-4681-a231-8a9bc9ca3402)


## full subtractor:

![image](https://github.com/22009011/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343461/3584b25d-c0ac-432b-bfca-f72fd9d5da53)



## Truthtable

## half subtractor:

![image](https://github.com/22009011/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343461/91902291-7ddc-4d55-bba5-098d3ccc9184)

## full subtractor:

![image](https://github.com/22009011/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343461/85c184ad-719a-4a51-91ce-3d5e9759790f)



## output waveform:

## half subtractor:

![image](https://github.com/22009011/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343461/d0b61360-5b3b-45fd-9c51-f3e96ee17a62)


## full subtractor:

![image](https://github.com/22009011/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343461/f19e0dd2-94ff-4866-b5ae-6fd2f7171adf)



## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
