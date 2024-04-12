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
## Full_adder

module fullas(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        
and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);
or(carry,w2,w3,w4);
endmodule

## Full_subtractor

module fullas1(a, b, bin, diff, borrow);
input a, b, bin;
output diff, borrow;
wire w1, w2, w3, w4;   
xor(w1, a, b);
xor(diff, w1, bin);
and(w2, w1, bin);
and(w3, a, ~b);
and(w4, ~b, bin);
or(borrow, w2, w3, w4);
endmodule

```


**RTL Schematic**

**Full Adder**

![Screenshot 2024-04-10 143526](https://github.com/DHIRAVIYASUNDARAM/FULL_ADDER_SUBTRACTOR/assets/165143880/652ca2dd-c2dd-49d3-8a5a-3da32f2b4dbf)

**Full Subtrator**

![Screenshot 2024-04-12 155213](https://github.com/DHIRAVIYASUNDARAM/FULL_ADDER_SUBTRACTOR/assets/165143880/858aca77-3bfb-4e5b-a70d-e3fc18bccca4)

**Output Timing Waveform**

**Full Adder**

![Screenshot 2024-04-10 161817](https://github.com/DHIRAVIYASUNDARAM/FULL_ADDER_SUBTRACTOR/assets/165143880/5579a3a5-55e6-47a1-beaa-447a37f51386)

**Full Subtrator**

![Screenshot 2024-04-12 155049](https://github.com/DHIRAVIYASUNDARAM/FULL_ADDER_SUBTRACTOR/assets/165143880/5181df21-0531-401c-a625-95f961e1bdcb)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



