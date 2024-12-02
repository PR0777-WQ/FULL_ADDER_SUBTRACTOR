![exp4a](https://github.com/user-attachments/assets/49b65f43-6fb6-4354-affb-fe8f0d780832)# FULL_ADDER_SUBTRACTOR

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
![full-adder-truth-table](https://github.com/user-attachments/assets/36701cff-b016-455f-a766-5ccd9361239f)

**Full Subtractor**
![full-subtractor-truth-table](https://github.com/user-attachments/assets/6cd786f9-a832-456f-88b1-26012cc317b9)

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

**Full Adder**
```
//full adder 
module exp4a(sum,cout,a,b,cin);
output sum;
output cout;
input a,b,cin;

//internal nets
wire s1,c1,c2;

//instantiate logic gate primitives
xor(s1,a,b);
and(c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c2);

endmodule
```

**Full Subtractor**
```
module exp4b(df,bo,a,b,bin);
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


Developed by: G Nitin Karthikeyan
RegisterNumber: 24010473
*/

**RTL Schematic**

**Full Adder**
![exp4a](https://github.com/user-attachments/assets/5451b860-5819-4221-98a2-7e1c5811292e)

**Full Subtractor**
![exp4b](https://github.com/user-attachments/assets/15b64264-8552-4b4a-a821-db9cc3f53fd9)

**Output Timing Waveform**

**Full Adder**
![Waveform result screenshot 4a](https://github.com/user-attachments/assets/1e1cf09d-ab10-48d3-ad9c-cd115202d644)

**Full Subtractor**
![Waveform result screenshot 4b](https://github.com/user-attachments/assets/cbfc1fff-3373-4976-be03-4b7fb5fd2b91)

**Result:**
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



