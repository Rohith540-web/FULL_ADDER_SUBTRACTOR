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


i)




![Screenshot 2024-12-06 195007](https://github.com/user-attachments/assets/1e128afd-9ef1-442a-af60-c19496af9d68)


ii)



![Screenshot 2024-12-06 195154](https://github.com/user-attachments/assets/7960e4a9-86ed-4343-be79-1688062f2ada)

**Procedure**

Write the detailed procedure here
Developed by:Rohith
Regester Number:24900447

**Program:**
```
i)FULL ADDER

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^c);
assign carry= ( (a & b)| ( cin &(a ^ b ));
endmodule

ii)FULL SUBTRACTOR

module fs(a,b,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b )));
endmodule




```


**RTL Schematic**

i)


![Screenshot 2024-12-06 114326](https://github.com/user-attachments/assets/9b497c24-7b27-47b0-a330-d888b3a06b03)



ii)


![Screenshot 2024-12-06 115413](https://github.com/user-attachments/assets/69358bff-e865-4098-b342-ab2da19247e2)

**Output Timing Waveform**
i)

![Screenshot (57)](https://github.com/user-attachments/assets/6a540833-c80a-40f2-b7df-cb664b354d15)


ii)
![Screenshot (58)](https://github.com/user-attachments/assets/d81303a1-a84d-4bc7-b824-223f9102809c)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



