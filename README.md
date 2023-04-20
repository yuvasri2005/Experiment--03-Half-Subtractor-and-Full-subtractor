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
WRITE THE DETAILED PROCEDURE HERE 


## Program:

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

HALF SUBTRACTOR

module HalfSub(a,b,difference,borrow);

input a,b;

output difference,borrow;

assign difference=(a^b);

assign borrow=(~a&b);

endmodule

FULL SUBTRACTOR

module FullSub(a,b,c,difference,borrow);

input a,b,c;

output difference,borrow;

assign borrow=(~a&(b^c)|(b&c));

assign difference=(a^b^c);

endmodule



Developed by: K.YUVASRI

RegisterNumber: 212222050061 


## Output

HALF SUBTRACTOR



![WhatsApp Image 2023-04-20 at 10 36 19 AM](https://user-images.githubusercontent.com/129949620/233266123-21b550f9-eabd-4d9d-b4d8-dc7cd6f67431.jpeg)


FULL SUBTRACTOR


![WhatsApp Image 2023-04-20 at 10 36 27 AM](https://user-images.githubusercontent.com/129949620/233266300-7c3b55b2-80df-4e71-a147-77e7855e243a.jpeg)






## Truthtable

HALF SUBTRACTOR

![WhatsApp Image 2023-04-20 at 10 49 04 AM](https://user-images.githubusercontent.com/129949620/233266535-188a2886-177e-4e32-aae5-f0e1022aba39.jpeg)


FULL SUBTRACTOR


![WhatsApp Image 2023-04-20 at 10 49 43 AM](https://user-images.githubusercontent.com/129949620/233266573-df8b3692-d275-4c6e-ae40-fc36c5bc0b43.jpeg)



##  RTL realization


## Timing diagram

HALF SUBTRACTOR




![WhatsApp Image 2023-04-20 at 10 36 38 AM](https://user-images.githubusercontent.com/129949620/233266445-e5bbb5f2-0818-45c8-a978-d2cc599ac72d.jpeg)


FULL SUBTRACTOR


![WhatsApp Image 2023-04-20 at 10 36 49 AM](https://user-images.githubusercontent.com/129949620/233266477-86051b1a-4be5-4d03-b666-19d584cf6420.jpeg)



## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
