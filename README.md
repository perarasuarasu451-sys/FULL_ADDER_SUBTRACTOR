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

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.



**Program:**

**Full adder**

```
module full_adder (
    input  wire a, b, cin,   // Inputs
    output wire sum, carry   // Outputs
);

    // Logic equations
    assign sum   = a ^ b ^ cin;                  // XOR for sum
    assign carry = (a & b) | (b & cin) | (a & cin); // Majority function for carry

endmodule

```

Program to design a full adder and full subtractor circuit and verify its truth table in quartus using Verilog programming.

<img width="857" height="243" alt="image" src="https://github.com/user-attachments/assets/70af2cc4-955a-4d80-9bde-3b74ab9f42ce" />

**Full subtractor**

```
module full_subtractor (
    input  wire a, b, bin,       // Inputs
    output wire diff, borrow     // Outputs
);

    // Logic equations
    assign diff   = a ^ b ^ bin;                  // Difference
    assign borrow = (~a & b) | (~(a ^ b) & bin);  // Borrow logic

endmodule
```

Program to design a full adder and full subtractor circuit and verify its truth table in quartus using Verilog programming.

<img width="717" height="250" alt="image" src="https://github.com/user-attachments/assets/313f7365-ec7e-4eca-b167-4d296534c049" />

Developed by: PERARASU K RegisterNumber: 25004665


**RTL Schematic**

**Full adder**
<img width="996" height="761" alt="image" src="https://github.com/user-attachments/assets/ccd43f58-e01e-45ef-9194-b8febd5dc44f" />

**Full subtractor**
<img width="1003" height="641" alt="image" src="https://github.com/user-attachments/assets/64744f68-bc21-4385-a2e7-71335c1b11ae" />

**Output Timing Waveform**

**Full adder**
<img width="1230" height="293" alt="image" src="https://github.com/user-attachments/assets/6d5fb8bf-1c1b-454f-b5b6-8a0e9ad08a38" />

**Full subtractor**
<img width="1230" height="293" alt="image" src="https://github.com/user-attachments/assets/9033c414-5df5-4454-af6b-d4c0b815beb6" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



