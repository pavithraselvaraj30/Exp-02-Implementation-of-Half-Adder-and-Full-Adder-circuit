## NAME:Pavithra.S
## Register number:212223230147

# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
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
### 
Program:
```
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by:Pavithra.S
RegisterNumber:212223230147
module half_adder(A,B,C,S);
input A,B;
output S,C;
assign c=A&B;
assign S=A^B;
endmodule


module FullAdder(a,b,carryin,sum,carryout);
input a,b,carryin;
output sum,carryout;
wire x,p,q,r;
xor(x,b,carryin);
xor(sum,x,a);
and(p,a,b);
and(q,b,carryin);
and(r,a,carryin);
or(carryout,p,q,r);
endmodule
*/
```
Logic symbol & Truthtable
## Half adder
![image](https://github.com/pavithraselvaraj30/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149366880/e7ece802-5ece-4a9c-a1d9-dee114a6bb21)

##  Full adder
![image](https://github.com/pavithraselvaraj30/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149366880/39e10a75-bafd-49d5-b922-b65915d86659)

## RTL realization
## Half adder
![image](https://github.com/pavithraselvaraj30/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149366880/8a01254d-8c9d-4a1b-a9d1-25ac73af3097)

## Full adder
![image](https://github.com/pavithraselvaraj30/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149366880/b66afc49-a53f-4de7-a63f-262036fd2709)



### TIMING DIAGRAM
## Half adder
![image](https://github.com/pavithraselvaraj30/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149366880/9da5e25f-4279-40d2-8927-23e518c75d8e)
Full adder
![image](https://github.com/pavithraselvaraj30/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/149366880/293e23cf-c02f-4dc1-98ba-eb7b4026ab6e)


### Result:
Thus the given logic functions are implemented and their operations are verified using verilog programming.
