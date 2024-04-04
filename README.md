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

**Truthtable:**
**Full Subtractor**
![image](https://github.com/jabezs2005/FULL_ADDER_SUBTRACTOR/assets/147473463/1f2e747a-4c6c-46d7-ad78-c8d080e83970)
**Half Subtractor**
![Screenshot 2024-04-04 140016](https://github.com/jabezs2005/FULL_ADDER_SUBTRACTOR/assets/147473463/b73023bb-276d-4b47-abb1-24364f4f0b0b)

**Procedure:**

**Create a new Quartus project:** Launch Quartus Prime software and create a new project. Provide a name for your project and specify the location where you want to save it.

**Design Entry:** In the Quartus software, go to File > New > Project Wizard. Follow the wizard to specify the target device family, device, and any other relevant settings.

**Create a schematic:** In Quartus, you can create a schematic using the built-in schematic editor. You'll need to design a circuit that includes full adders and logic gates to handle subtraction. Alternatively, you can write Verilog or VHDL code for your full adder/subtractor.

**Write Verilog or VHDL code:** Open a new file in Quartus and write the Verilog or VHDL code for your full adder/subtractor.

**Compile the design:** After designing your circuit or writing the Verilog/VHDL code, compile your design by clicking on Processing > Start Compilation.

**Simulate your design:** You can simulate your design using ModelSim, which is included with Quartus. This helps you verify that your design functions correctly.

**Program your FPGA:** Once your design is successfully compiled and simulated, you can program your FPGA using the Programmer tool in Quartus.

**Test your design:** After programming the FPGA, you can test your full adder/subtractor to ensure it behaves as expected.

**Program:**
**Full Subtractor**
```
module exmp4(df,bo,a,b,bin);
output df,bo;
input a,b,bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule
```
**Half Subtractor**
```
module exmp4 (df,bo,a,b);
output df,bo;
input a,b;
assign df=a^b;
assign bo=(~a&b);
endmodule
```

**RTL Schematic**
**Full Sbtractor**
![Screenshot 2024-04-04 133649](https://github.com/jabezs2005/FULL_ADDER_SUBTRACTOR/assets/147473463/38e6c022-fc23-4793-af59-00eaaf5f6444)
**Half Subtractor**
![Screenshot 2024-04-04 140016](https://github.com/jabezs2005/FULL_ADDER_SUBTRACTOR/assets/147473463/ea9eedc3-715e-4075-bf7a-dcd2435faaa8)

**Output Timing Waveform**
**Full Subtractor**
![Screenshot 2024-04-04 133543](https://github.com/jabezs2005/FULL_ADDER_SUBTRACTOR/assets/147473463/148b6595-d66c-4c59-8269-20f448e6d065)
**Half Subtractor**
![Screenshot 2024-04-04 135929](https://github.com/jabezs2005/FULL_ADDER_SUBTRACTOR/assets/147473463/84ef5a76-dd42-4ba3-8bbb-3769dd5b3bd0)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



