
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
![fulladder](https://github.com/user-attachments/assets/f2fdfea4-d6f6-40aa-b5a2-5a3e8ce8038a)
![fullsub](https://github.com/user-attachments/assets/94fcfe80-6ea9-4957-bf9a-bfea44185c75)


**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: 
*/
```
RegisterNumber:212224040036
Name:Asin Renix V
```

```
FULL SUBTRACTER:
module fullsub(df, bo, a, b, bin);
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
FULL ADDER:
module fulladd(sum, cout, a, b, cin);
    output sum;
    output cout;
    input a;
    input b;
    input cin;

	 wire w1,w2,w3;
	 assign w1=a^b;
	 assign w2=a&b;
	 assign w3=w1&cin;
	 assign sum=w1^cin;
	 assign cout=w2|w3;
endmodule
```

**RTL Schematic**
![Screenshot (3)](https://github.com/user-attachments/assets/6c61fd53-91af-422b-bc9b-c0d6acb0ccff)
![Screenshot (5)](https://github.com/user-attachments/assets/d650961c-7422-4e1d-b68a-a1da2191973d)


**Output Timing Waveform**
![Screenshot (4)](https://github.com/user-attachments/assets/84ec9171-0d78-4ca0-8c30-47c911e84c4a)
![Screenshot (6)](https://github.com/user-attachments/assets/5afc5a15-e805-4b2c-a94f-da14adc8b54c)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



