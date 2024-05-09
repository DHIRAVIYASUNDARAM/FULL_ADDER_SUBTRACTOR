# DEVELOPED BY : DHIRAVIYA S
# REGISTER NO: 212223040041
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

**Full Adder**

![Screenshot 2024-04-10 134929](https://github.com/DHIRAVIYASUNDARAM/FULL_ADDER_SUBTRACTOR/assets/165143880/eaf33e90-34e1-41c7-871d-dee563b66d5c)

**Full Subractor**

![Screenshot 2024-04-10 135121](https://github.com/DHIRAVIYASUNDARAM/FULL_ADDER_SUBTRACTOR/assets/165143880/b9fb08f8-ae9c-40ca-b7bc-70db7c9c8835)


**Procedure**

**Full Adder:**

1.Open Quartus II and create a new project.

2.Use schematic design entry to draw the full adder circuit. 

3.The circuit consists of XOR, AND, and OR gates. 

4.Compile the design, verify its functionality through simulation. 

5.Implement the design on the target device and program it.

**Full Subtractor:** 

1.Follow the same steps as for the full adder. 

2.Draw the full subtractor circuit using schematic design. 

3.The circuit includes XOR, AND, OR gates to perform subtraction. 

4.Compile, simulate, implement, and program the design similarly to the full adder.

**Program:**

```
module FullAddSub(a,b,c,sum,carry,D,BO);
input a,b,c;
output sum,carry,D,BO;
assign sum=a^b^c;
assign carry=(a&b)|(b&c)|(a&c);
assign D=a^b^c;
assign BO=(~a&b)|(b&c)|(~a&c);
endmodule

```


**RTL Schematic**

![image](https://github.com/DHIRAVIYASUNDARAM/FULL_ADDER_SUBTRACTOR/assets/165143880/f25fb961-f5a3-4bf2-bad9-529c9f5b28db)


**Output Timing Waveform**

![image](https://github.com/DHIRAVIYASUNDARAM/FULL_ADDER_SUBTRACTOR/assets/165143880/76ef9e6e-7ed4-47cf-9bd9-337bc7da5dc7)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



