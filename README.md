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

FULL ADDER

![image](https://github.com/user-attachments/assets/a8cd6506-dfd0-4aa0-b772-7d70d6857642)

FULL SUBTRACTOR

![image](https://github.com/user-attachments/assets/922e5afd-b12e-4ece-8044-4f8490341b51)


**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram

**Program:**


DEVELOPED BY: L INDHUMATHI


REGISTER NUMBER: 24900500

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
```
module exp4(a,b,c,sum,carry,BO,DIFF);

input a,b,c;

output sum,carry,BO,DIFF;

wire abar;

not (abar,a);

assign sum=a^b^c; 

assign carry=(a&b)|(a&c)|(b&c);

assign diff=a^b^c;

assign BO=(~a&b)|(~a&c)|(b&c);

endmodule
```
**RTL Schematic**

![Screenshot 2024-12-03 211827](https://github.com/user-attachments/assets/70059e97-782f-4e12-93c1-bf4e2754021f)


**Output Timing Waveform**

![Screenshot 2024-12-03 212127](https://github.com/user-attachments/assets/46dc1333-61c8-4b16-bd62-e5752789a019)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



