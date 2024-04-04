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
![image](https://github.com/SJananisenthilkumar/FULL_ADDER_SUBTRACTOR/assets/144871139/7c333ca4-05d4-4750-b576-001e54053e2d)
**Full Subractor**
![image](https://github.com/SJananisenthilkumar/FULL_ADDER_SUBTRACTOR/assets/144871139/4592159c-bed6-438f-9408-25266fc0d0e2)

**Procedure**
1.Use module projname(input,output) to start the Verilog programming. 
2.Assign inputs and outputs using the word input and output respectively. 
3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression. 
4.Use each output to represent one for difference and the other for borrow. 
5.End the verilog program using keyword endmodule

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/
```
module fulladd_top(a,b,cin,sum,carry);
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
```
**Full Subractor**
```
module fullsub_top(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
  assign BO = (a & b) | ((a ^ b) & Bin);
endmodule
```
**RTL Schematic**
![image](https://github.com/SJananisenthilkumar/FULL_ADDER_SUBTRACTOR/assets/144871139/c6ef190a-d28d-4e35-8e6f-6e3605e6a7f3)
**Full Subractor**
![image](https://github.com/SJananisenthilkumar/FULL_ADDER_SUBTRACTOR/assets/144871139/c533cceb-3814-483b-8bf6-c839b9085105)

**Output Timing Waveform**
![image](https://github.com/SJananisenthilkumar/FULL_ADDER_SUBTRACTOR/assets/144871139/2eba5cc6-86a6-4bc7-975e-62b1c1925228)
**Full Subractor**
![image](https://github.com/SJananisenthilkumar/FULL_ADDER_SUBTRACTOR/assets/144871139/faf9b50f-9164-4de2-b390-f53fdfe28dd6)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



