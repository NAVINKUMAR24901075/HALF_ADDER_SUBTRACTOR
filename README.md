## NAME: S.NAVINKUMAR
## REG.NO: 24901075
# EXPERIMENT-3: IMPLEMENTATION OF HALF ADDER AND SUBTRACTOR

# AIM:
To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

# EQUIPMENTS REQUIRED:
Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

# HALF ADDER:

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

# HALF SUBTRACTOR:

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

# PROCEDURE

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


# PROGRAM:
~~~~~~
module halfaddsub(a,b,sum,carry,difference,borrow);
input a,b;
output sum,carry,difference,borrow;
assign sum=a^b;
assign carry=a&b;
assign difference=a^b;
assign borrow=(~a)&b;
endmodule
~~~~~~

# TRUTH TABLE:

![Screenshot 2024-11-08 094724](https://github.com/user-attachments/assets/d24db141-d60d-4843-9ba3-7933affe38c6)

![Screenshot 2024-11-08 094741](https://github.com/user-attachments/assets/175de606-794f-44a2-b498-6fea2b2bd175)


# RTL OUTPUT:

![Screenshot 2024-11-14 030913](https://github.com/user-attachments/assets/2c46ef35-d1f4-4d18-b956-82b977a182c0)

# OUTPUT WAVEFORM:

![Screenshot 2024-11-14 031935](https://github.com/user-attachments/assets/7fdf9855-cc2e-45b2-9ece-dd6b1c62b87e)

# RESULT:

Designed a half adder and half subtractor circuit and verified its truth table in Quartus using Verilog programming
