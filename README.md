# FULL_ADDER_SUBTRACTOR
```
Developed by:Preethi.K
RegisterNumber: 212224240118
```
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

![Screenshot 2025-04-23 160218](https://github.com/user-attachments/assets/d5054afc-294f-4ffc-8ef8-325296f687d4)
![Screenshot 2025-04-23 160227](https://github.com/user-attachments/assets/1acb3624-5724-4eb4-b7d3-a82098790cfe)


**Procedure**
```
  1.Type the program in Quartus software.
  2.Compile and run the program.
  3.Generate the RTL schematic and save the logic diagram.
  4.Create nodes for inputs and outputs to generate the timing diagram.
  5.For different input combinations generate the timing diagram.
```
**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
```
FULL ADDER

module FH(a,b,c,sum, carry);
input a,b,c;
output sum, carry;
wire w1,w2,w3;
assign sum=a^b^c;
assign w1=a&b;
assign w2=b&c;
assign w3=c&a;
assign carry=w1|w2|w3;
endmodule;

FULL SUBTRACTOR

module FH(difference, borrow, a, b, bin);
input a,b,bin;
output differencef,borrow;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign difference=w1^bin;
assign borrow=w2|w3;
endmodule;
```

**RTL Schematic**

![Screenshot 2025-04-23 160301](https://github.com/user-attachments/assets/b0b5e839-e6b0-44a1-8f3f-224db42f58be)
![Screenshot 2025-04-23 160312](https://github.com/user-attachments/assets/e0d765d8-491b-4a1a-be19-0f74ad695f31)


**Output Timing Waveform**

![Screenshot 2025-04-23 160325](https://github.com/user-attachments/assets/c4236975-3990-4877-98e4-4c73ac9175c3)
![Screenshot 2025-04-23 160338](https://github.com/user-attachments/assets/1e8b38ff-b0f2-4ae7-8feb-c84cd9261ae3)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



