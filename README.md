# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

FULLADDER:

![image](https://github.com/SridharShyam/FULL_ADDER_SUBTRACTOR/assets/144871368/f9d9844a-fd6b-4e04-adcf-00b6b99c4407)

FULLSUBTRACTOR:

![image](https://github.com/SridharShyam/FULL_ADDER_SUBTRACTOR/assets/144871368/3bcd30a4-57b2-4f4e-95e5-ea60da8d8899)



**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/
```
FULLADDER:

module fulladder(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        
and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);
or(carry,w2,w3,w4);
endmodule

FULLSUBTRACTOR:

module fullsub_top(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
  assign BO = (a & b) | ((a ^ b) & Bin);
endmodule
```

**RTL Schematic**

FULLADDER:

![Screenshot 2024-03-19 085835](https://github.com/SridharShyam/FULL_ADDER_SUBTRACTOR/assets/144871368/93a676fe-5ce9-4a7f-a2c0-6b0bf8494caa)

FULLSUBTRACTOR:

![Screenshot 2024-03-20 201226](https://github.com/SridharShyam/FULL_ADDER_SUBTRACTOR/assets/144871368/00c6fa7b-b753-48ce-a139-80ec62d1955d)

**Output Timing Waveform**

FULLADDER:

![Screenshot (92)](https://github.com/SridharShyam/FULL_ADDER_SUBTRACTOR/assets/144871368/6fc891f2-81a6-412d-a061-ffb2999691a6)

FULLSUBTRACTOR:

![WhatsApp Image 2024-03-21 at 09 41 20_d31066f0](https://github.com/SridharShyam/FULL_ADDER_SUBTRACTOR/assets/144871368/b641ede3-dd97-401e-9e99-56c3e123e0b2)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



