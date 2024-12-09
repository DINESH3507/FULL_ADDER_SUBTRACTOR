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

![Screenshot 2024-12-09 180100](https://github.com/user-attachments/assets/eecccdf2-a415-43c5-95d8-36d6498fc10d)


**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![Screenshot 2024-12-09 181656](https://github.com/user-attachments/assets/c060e829-6542-4b4f-89af-d5addf7e57fa)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 


Developed by: Dinesh.V

RegisterNumber: 24010667

module fulladder(a,b,cin,sum,carry);

input a,b,cin;

output sum,carry;

assign sum=(a^b^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

endmodule

module fullsubtractor(a,b,bin,difference,borrow);

input a,b,bin;

output difference,borrow;

assign difference= (a^b^bin);

assign borrow=(~a&b)|(bin & ~(a^b));

endmodule

**RTL Schematic**

![Screenshot 2024-12-09 180254](https://github.com/user-attachments/assets/3fe55514-3d1f-445a-be4b-36f7462932d4)

![Screenshot 2024-12-09 182000](https://github.com/user-attachments/assets/ae373a24-c0a9-487c-9f45-d181fe650c47)

**Output Timing Waveform**

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



