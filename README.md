## Name: Yashvanth K
## Reference number:23011613
# Exp 03 Implementation of Half Adder and Full Adder circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime
## Theory
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
### Half Adder Program:
```
module fulladder(sum,a,b,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
```
### Full Adder Proogram:
```
module fulladder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor(sum,a,b,c);
assign carry=a&b | b&c | a&c;
endmodule
```
### RTL realization
#### Half Adder:
![experiment3 halfadder RTL](https://github.com/Ashwathm12/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/138849225/f6d308a8-a007-4c50-9b77-2e0eb6b2d3e8)

#### Full Adder:
![experiment3 fulladder rtl](https://github.com/Ashwathm12/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/138849225/80c6acb0-94cc-4fb6-b9e7-b80695831fc2)

### Truth table:
#### Half Adder:
![experiment3 halfadder truthtable](https://github.com/Ashwathm12/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/138849225/eb5a81d3-00af-4155-b4bb-a2a861bcc62f)

#### Full Adder:
![experiment3 fulladder truthtable](https://github.com/Ashwathm12/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/138849225/ef0468bd-87c5-40e8-ae4c-b862c95cf2cc)

### Timing Diagram
#### Half Adder:
![experiment3 halfadder diagram](https://github.com/Ashwathm12/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/138849225/ed797cef-2726-4b9b-9dcb-3c6249a7f4df)

#### Full Adder:
![experiment3 fulladder diagram](https://github.com/Ashwathm12/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/138849225/93e0fd62-c414-4b10-b268-18ff12869e34)


### Result:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.
