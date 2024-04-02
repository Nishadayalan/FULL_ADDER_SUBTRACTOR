# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor:**

**Full Adder:**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER:**

**Full Subtractor:**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable:**

![image](https://github.com/Nishadayalan/FULL_ADDER_SUBTRACTOR/assets/144870468/a623ed6b-209b-40dd-b52a-b4c6748b2f60)



**Procedure**

1.Open Quartus II & create a new project and then type the program in Quartus software.

2.Compile and run & save the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

6.Verify its functionality through simulation.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
### Developed by: NISHA.D
### RegisterNumber: 212223230143

```

module FULLADDSUB(a,b,c,sum,carry,D,BO);
input a,b,c;
output sum,carry,D,BO;
assign sum=a^b^c;
assign carry=(a&b)|(b&c)|(a&c);
assign D=a^b^c;
assign BO=(~a&b)|(b&c)|(~a&c);
endmodule

```

![image](https://github.com/Nishadayalan/FULL_ADDER_SUBTRACTOR/assets/144870468/498a0876-ff74-4e8f-8460-07714b2e2a1d)


**RTL Schematic:**

![image](https://github.com/Nishadayalan/FULL_ADDER_SUBTRACTOR/assets/144870468/7e09d050-1020-4528-b927-3e9964dd8036)


**Output Timing Waveform:**
![image](https://github.com/Nishadayalan/FULL_ADDER_SUBTRACTOR/assets/144870468/47fd7700-d751-4103-b49e-e5688df760ab)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



