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
![image](https://github.com/user-attachments/assets/d1d53c46-a354-4a16-b7d7-5dd347b47cad)
![image](https://github.com/user-attachments/assets/194003cd-37d8-49d7-9407-ce8cf86e9d3a)

**Procedure**

Create a New Project:

Open Quartus.
Start a new project and name it (e.g., FullAdderSubtractor).
Write the Verilog Code:

Create two separate Verilog files, one for the Full Adder (FullAdder.v) and another for the Full Subtractor (FullSubtractor.v).
Copy and paste the provided Verilog code into each file.
Compile the Design:

Compile both files to ensure there are no syntax errors.


**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/
i)FULL ADDER
```
module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^c);
assign carry= ( (a & b)| ( cin &(a ^ b ));
endmodule
```
ii)FULL SUBTRACTOR
```
module fs(a,b,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b )));
endmodule
```

**RTL Schematic**
![image](https://github.com/user-attachments/assets/7ac0fb28-dab6-47d8-9428-5a80e6712c88)
![image](https://github.com/user-attachments/assets/46254c9c-0e95-4d15-8608-983205efdfd0)

**Output Timing Waveform**
![exp 4 1 A](https://github.com/user-attachments/assets/693e2eff-3186-4a12-bbf0-2bcd39554cce)
![ep 4 1B](https://github.com/user-attachments/assets/b85008b7-03c7-44d8-99ac-ce383bf9c9f4)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



