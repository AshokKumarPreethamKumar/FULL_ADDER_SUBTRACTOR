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

![FA Truthtable](https://github.com/user-attachments/assets/8057e6e7-c6af-486c-a170-1dcb9d11fff1)

FULL SUBTRACTOR

![FS Truthtable](https://github.com/user-attachments/assets/662a0bec-d3e1-4e2b-bdd7-c5094c76ca2d)



**Procedure**

1. Type the program in Quartus software.
2. Compile and run the program.
3. Generate the RTL schematic and save the logic diagram.
4. Create nodes for inputs and outputs to generate the timing diagram.
5. For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.*/

FULL ADDER

```
module exp4fulladder(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
```

FULL SUBTRACTOR

```
module exp4fullsubtractor(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
```


Developed by: ASHOK KUMAR PREETHAM KUMAR

RegisterNumber:24002459


**RTL Schematic**

FULL ADDER

![exp4fulladder](https://github.com/user-attachments/assets/f83076a1-6f61-4e0c-bf0c-66423113a578)

FULL SUBTRACTOR

![exp4fullsubtractor](https://github.com/user-attachments/assets/ae575957-0eec-4a5e-a3d2-ee4db335bce5)



**Output Timing Waveform**

FULL ADDER

![FA timing waveform](https://github.com/user-attachments/assets/4139dde4-c5d8-46c7-a17d-507c1e0c961f)

FULL SUBTRACTOR

![FS timing waveform](https://github.com/user-attachments/assets/65d68ce8-4fb6-4ec6-a9b7-fcf9946200e3)





**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



