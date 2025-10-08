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
fulladder
<img width="1167" height="663" alt="image" src="https://github.com/user-attachments/assets/986f13ad-6a56-4dd8-afec-1f290e6f9181" />
fullsubtractor
<img width="1140" height="673" alt="image" src="https://github.com/user-attachments/assets/dc300782-f3c4-48bd-b1a4-c829788cd0cf" />

**Procedure**

Write the detailed procedure here

**Program:**
fulladder
```module fulladder(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

```
fullsubtractor
```module fullsubtractor(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule


```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL Schematic**
fulladder
<img width="1920" height="1080" alt="Screenshot (89)" src="https://github.com/user-attachments/assets/05ae2eb1-4ef6-4cac-970a-881884e9d63a" />
fullsubtractor
<img width="1920" height="1080" alt="Screenshot (89)" src="https://github.com/user-attachments/assets/d2c18afc-2ecf-415a-805f-477aab233e2e" />

**Output Timing Waveform**
fulladder
<img width="1920" height="1080" alt="Screenshot (90)" src="https://github.com/user-attachments/assets/21b6d06e-ce6e-4595-a9d5-5c70352c813c" />
fullsubtractor
<img width="1920" height="1080" alt="Screenshot (92)" src="https://github.com/user-attachments/assets/e21bcde7-35e9-423a-9786-8d9ee37257ee" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



