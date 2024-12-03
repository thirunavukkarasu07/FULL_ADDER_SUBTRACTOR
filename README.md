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

![WhatsApp Image 2024-12-03 at 5 01 08 PM](https://github.com/user-attachments/assets/013d98f2-6c55-4f59-b012-3d814b014521)


FULL SUBRACTOR

![WhatsApp Image 2024-12-03 at 5 02 35 PM](https://github.com/user-attachments/assets/98e2e281-8030-45c7-a470-297972157dd4)


**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.


**Program:**

FULL ADDER 
```
module exp4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
wire s1,c1,c2;
xor(s1,a,b);
and(c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c1);
endmodule
```

FULL SUBRACTOR
```
module exp4a(df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule
```


/* Program to design a full adder and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by:THIRUNAVUKKARASU MEENAKSHISUNDARAM 
RegisterNumber:24006365
*/

**RTL Schematic**

FULL ADDER 

![WhatsApp Image 2024-12-03 at 4 33 25 PM](https://github.com/user-attachments/assets/e8d04f1a-3477-4bf7-967d-377a523502ec)


FULL SUBRACTOR
![WhatsApp Image 2024-12-03 at 4 41 13 PM](https://github.com/user-attachments/assets/195a2d88-8771-4088-bf5e-2e0aab463fa0)


**Output Timing Waveform**

FULL ADDER

![WhatsApp Image 2024-12-03 at 4 33 43 PM](https://github.com/user-attachments/assets/8ddcd88b-cf7f-4e9b-a404-6babac518b6d)

FULL SUBRACTOR

![WhatsApp Image 2024-12-03 at 4 44 14 PM](https://github.com/user-attachments/assets/056b4368-3c85-4516-983c-9797db37bcb3)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



