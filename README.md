# Binary-Mini-Calculator
Project Report – Mini Calculator ( 4-bits Calculator)
Lecture: Computer Architecture
Lecturer: Lay Vathana
Team Member: 
- Chhort Chhorraseth @
- Keb Sreynaj @kebsreynaj2@gmail.com
- Oeun Panhayuth - @lorena.kreiger8@gmail.com
- Phan Reach - @reach4phan@gmail.com


# Introduction/Objectives
The mini calculator logic gate circuit project aims to implement basic arithmetic operations (addition, subtraction, multiplication, and division) using logic gates such as AND, OR, XOR, and NOT gates. This report outlines the implementation details, including truth tables and circuit diagrams, for each operation.


 # Addition Operation
	To build an 8-bits addition circuit, we'll need to cascade 1 half-adder and 7 full-adders together.
Let's start by designing a half adder, which adds two single binary digits (0 or 1) and produces the sum and carry out. Then, we'll extend it to a full adder, which adds two bits along with a carry-in and produces a sum and carry-out.


## 2.1 Half-Adder
A half-adder takes two inputs (A and B) and produces two outputs: the sum (S) and the carry ( C ).
 In this case,
XOR gate is used to provide the sum of input
AND gate provides the carry of the input
By combining these 2, we get both the sum and the carry.


## Truth Table (Half-Adder)

Based on truth table we minimize our variables to:
	Sum= A XOR B = A⊕B
	Carry = A AND B = A*B
Logic circuit (Half-Adder) 

## 2.2 Full Adder
Take two inputs A and B, and the other one is the carry that was obtained from the previous addition as C-IN. It designates the input carry as the C-OUT and the normal output as S, or sum.
A full adder is a circuit that has two AND gates, two EX-OR gates, and one OR gate. The full adder adds three binary digits.
Truth Table(Full Adder)

K-Map and Logic Expression of Full Adder





This is our integrated circuit for half-adder and full adder:


(Full-adder) 						(Half-Adder)







## Logic circuit 4 bits addition(Full Adder)





As we now have our integrated circuit of full and half adder, let's build our 8-bits addition circuit:
_ Input: we have two 8-bits binary inputs (X and Y) to be added.
_ Build half-adder: Use half-adder to add the least significant bits of the two input X0 and Y0.
Then we use full-adder for the 7 remaining bits, considering the carry from the previous process
_ Cascade Adders: Connect the outputs (sum and carry-out) of each adder to the inputs (A, B, and carry-in) of the next adder.

# 3.0 subtractor operation 
# 3.1 Half subtraction
	A half-subtractor circuit is used to perform a binary subtraction of two single-bit binary numbers and it has two inputs, A and B , and two outputs, DIFFERENCE and BORROW. 
## Truth table 

Diff = A’B + AB’
Borrow = A’B
Logic circuit 



## 3.2 Full Subtractor
	A full subtractor is a combination of circuits that performs subtraction of two bits. This circuit has three inputs and two outputs. The three inputs A, B and Bin, denote the minuend, subtrahend, and previous borrow, respectively. The two outputs, D and Bout represent the difference and output borrow.   
Truth table


## Logic circuit for full subtractor





