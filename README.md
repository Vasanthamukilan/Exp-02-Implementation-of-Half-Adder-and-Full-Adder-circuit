# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
## AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

## Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

## Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure
Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
## Program:
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by:Vasanthamukilan.M 
RegisterNumber:212222230167

HALF ADDER:
module halfadder(A,B,C,S);
input A,B;
output S,C;
xor(S,A,B);
and(C,A,B);
endmodule

FULL ADDER:
module fulladd(a,b,ci,s,co);
input a,b,ci;
output s,co;
wire d,e,f;
xor(d,a,b);
xor(s,d,ci);
and(e,ci,d);
and(f,a,b);
or(co,e,f);
endmodule
```
## Output:
## RTL realization
### HALF ADDER
![Screenshot 2023-04-09 182511](https://user-images.githubusercontent.com/119559694/230773843-2b557587-31ff-4242-aba7-a7e37a4d0be9.png)
### FULL ADDER
![Screenshot 2023-04-09 184340](https://user-images.githubusercontent.com/119559694/230774718-2d262c4d-b83b-4e1d-979c-e027b11033ce.png)

## TIMING DIAGRAM:
### HALF ADDER
![Screenshot 2023-04-05 144931](https://user-images.githubusercontent.com/119559694/230773989-08f93014-f001-4699-b135-1db9bb937524.png)
### FULL ADDER
![Screenshot 2023-04-06 102836](https://user-images.githubusercontent.com/119559694/230774051-89cf7d76-b536-45db-9b62-e2604b405309.png)
## TRUTH TABLE: 
### HALF ADDER
![truthtable_half](https://user-images.githubusercontent.com/119559694/230774430-43cf1d7b-42e1-42bb-88a6-115877e00031.png)
### FULL ADDER
![truthtable_full (1)](https://user-images.githubusercontent.com/119559694/230774442-41633bca-f615-46e7-b405-ef31b8fa8c42.png)
### Result:
Thus the half adder and full adder are studied and the truth table for different logic gates are verified.
