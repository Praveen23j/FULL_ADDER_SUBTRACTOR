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
![384860192-b0bb3840-3918-413e-a873-6590b99eeac5](https://github.com/user-attachments/assets/90788abf-e155-4e81-8bfd-1d9a6cde43cd)

**Truthtable**
![384860286-8b03168c-0b03-461a-846d-45bcf690586b](https://github.com/user-attachments/assets/b2909f47-359f-49b5-ab50-8f1fcdd601df)

**Procedure**

Write the detailed procedure here
1.Write the code in Quartus software by creating a new project wizard. 2.Run the program to get output. 3.Then open RTL viewer and download that image. 4.Open new file with University program VWF 5.Set end timer and execute, then download the waveform.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

//full adder module EXP_4(sum, cout, a, b, cin); output sum; output cout; input a; input b; input cin; //internal nets wire sl,cl,c2; //Instantiate logic gate primitives xor (sl,a,b); and(cl,a,b); xor(sum, sl, cin); and (c2, sl,cin); or (cout, c2,cl); endmodule

module EXP_4_2 (df, bo, a, b, bin); output df; output bo; input a; input b; input bin; wire w1,w2,w3; assign w1=a^b; assign w2=(~a&b); assign w3=(~w1&bin); assign df=w1^bin; assign bo=w2|w3; endmodule

Developed by: RegisterNumber:
*/24900824

**RTL Schematic**
![384911902-c55a99ed-01c9-4805-a803-4a194802a563](https://github.com/user-attachments/assets/1a838d28-1644-48e8-85fb-9981e7f1dfb1)
![384912106-2afdd44f-200c-4a62-a464-f914709b5ab8](https://github.com/user-attachments/assets/5e9534a0-cb58-4e61-8474-b21ad815d68c)

**Output Timing Waveform**
![384912186-a5ceeb55-be23-4794-a97a-83297e2f6046](https://github.com/user-attachments/assets/62813e23-7377-4318-b215-888fd014f030)
![384912216-1ca8f530-7dd9-4e43-b592-cebb1a12aec7](https://github.com/user-attachments/assets/84b13751-a005-4d8f-adc5-ce17185ff732)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



