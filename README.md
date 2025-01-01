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

**Procedure**

1. Type the program in Quartus software.

2. Compile and run the program.

3. Generate the RTL schematic and save the logic diagram.

4. Create nodes for inputs and outputs to generate the timing diagram.

5. For different input combinations generate the timing diagram.

**Program:**

Half adder program:

module fulladd (

input a,b,c,

output sum,carry);

wire w1,w2,w3;

assign sum=a^b^c;

assign w1=a&b;

assign w2=b&c;

assign w3=c&a;

assign carry=w1|w2|w3;

endmodule

Full subtractor program:

module fullsub(a,b,c,diff,borr);

input a,b,c;

output diff,borr;

wire w1,w2,w3,w4,w5,w6;

xor g1(diff,a,b,c);

and g2(w4,w1,b);

and g3(w5,w1,b);

and g4(w6,b,c);

or g5(borr,w4,w5,w6);

endmodule


**RTL Schematic**

![Screenshot 2025-01-01 093232](https://github.com/user-attachments/assets/aeaeeb1e-af31-4ef2-8743-a1d301ce049d)

![Screenshot 2025-01-01 093256](https://github.com/user-attachments/assets/ecdc6865-1a0b-4e2c-aa9c-58952021a1f8)


**Output Timing Waveform**

![Screenshot 2025-01-01 093537](https://github.com/user-attachments/assets/ba34dfe5-12d9-42c4-a76b-21e9dc5f5c4a)

![Screenshot 2025-01-01 093504](https://github.com/user-attachments/assets/c81ee117-2709-4acb-9732-a7bebfc0b5fc)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



