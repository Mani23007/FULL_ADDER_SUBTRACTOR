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
![full_adder_tt](https://github.com/user-attachments/assets/599e03a9-a805-4450-b98f-090ef033a751)
![WhatsApp Image 2024-11-18 at 14 30 05_c991541b](https://github.com/user-attachments/assets/b55d1ad8-bfbd-46b9-b639-14633aa60cf1)

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: Manikandan RegisterNumber: 24900685
*/
 module unit22(sum,cout,a,b,cin);
 output sum;
 output cout;
 input a;
 input b;
 input cin;
 wire s1,c1,c2;
 xor (s1,a,b);
 and(c1,a,b);
 xor(sum,s1,cin);
 and(c2,s1,cin);
 or(cout,c2,c1);
 endmodule
 module unit23 (df,bo,a,b,bin);
 output df;
 output bo;
RTL Schematic
 Output Timing Waveform
 input a
**RTL Schematic**
![RTL Exp5](https://github.com/user-attachments/assets/6d4f9862-7a9e-44be-84a8-bf38f778a639)
![WhatsApp Image 2024-11-18 at 14 13 46_134608ca](https://github.com/user-attachments/assets/95eb7a07-88ae-4ff6-bf84-0ba60eddbfee)

**Output Timing Waveform**
![Screenshot 2024-11-18 141007](https://github.com/user-attachments/assets/fbf4fa67-4d40-49c2-84fc-039aab1ca26f)
![WhatsApp Image 2024-11-18 at 14 13 46_e63be326](https://github.com/user-attachments/assets/c11e2411-2d13-415c-8f89-039bc14e8a0b)

**Result:**
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



