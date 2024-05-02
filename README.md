# Binary-Mini-Calculator
Project Report – Mini Calculator ( 4-bits Calculator)

Lecture: Computer Architecture

Lecturer: Lay Vathana

Team Member: 
- Chhort Chhorraseth @chhortchhoraseth@gmail.com
- Keb Sreynaj @kebsreynaj2@gmail.com
- Oeun Panhayuth - @lorena.kreiger8@gmail.com
- Phan Reach - @reach4phan@gmail.com


# I. Introduction/Objectives
The mini calculator logic gate circuit project aims to implement basic arithmetic operations (addition, subtraction, multiplication, and division) using logic gates such as AND, OR, XOR, and NOT gates. This report outlines the implementation details, including truth tables and circuit diagrams, for each operation.


 # II. Addition Operation
To build an 4-bits addition circuit, we'll need to cascade 1 half-adder and 3 full-adders together.
Let's start by designing a half adder, which adds two single binary digits (0 or 1) and produces the sum and carry out. Then, we'll extend it to a full adder, which adds two bits along with a carry-in and produces a sum and carry-out.

## 2.1 Half-Adder
A half-adder takes two inputs (A and B) and produces two outputs: the sum (S) and the carry ( C ).
In this case, **XOR** gate is used to provide the sum of input **AND** gate provides the carry of the input
By combining these 2, we get both the sum and the carry.

### Truth Table (Half-Adder)
<img width="411" alt="image" src="https://github.com/Sreynaj/Binary-Mini-Calculator/assets/101303611/2699b518-38ec-4fcc-8c85-279739ab084b">

Based on truth table we minimize our variables to:
- Sum= A XOR B = A⊕B
- Carry = A AND B = A*B
Logic circuit (Half-Adder) 
<img width="411" alt="image" src="https://github.com/Sreynaj/Binary-Mini-Calculator/assets/101303611/dafb15bc-21a9-4ed3-8c9c-54b765c53cff">

## 2.2 Full Adder
Take two inputs A and B, and the other one is the carry that was obtained from the previous addition as C-IN. It designates the input carry as the C-OUT and the normal output as S, or sum. A full adder is a circuit that has two **AND** gates, two **EXOR** gates, and one **OR** gate. The full adder adds three binary digits.

###Truth Table: (Full Adder)

<img width="411" alt="image" src="https://github.com/Sreynaj/Binary-Mini-Calculator/assets/101303611/d8f2979c-6542-4caa-9b16-75907cd8b1c6">

### K-Map and Logic Expression of Full Adder

<img width="411" alt="image" src="https://github.com/Sreynaj/Binary-Mini-Calculator/assets/101303611/b18839d5-787a-4e72-bb5a-0599478869bb">

### This is our integrated circuit for half-adder and full adder:
- Half adder
<img width="411" alt="image" src="https://github.com/Sreynaj/Binary-Mini-Calculator/assets/101303611/544499d3-98b0-4365-a2f8-3122ff4bfcc2">


- Full adder
<img width="411" alt="image" src="https://github.com/Sreynaj/Binary-Mini-Calculator/assets/101303611/e9aed53b-e1ba-4866-9e64-316c303e8e8f">
 

## Logic circuit 4 bits addition(Full Adder)
<img width="711" alt="image" src="https://github.com/Sreynaj/Binary-Mini-Calculator/assets/101303611/2fe1a4a1-ca8d-4505-b04d-c893464a5e22">



As we now have our integrated circuit of full and half adder, let's build our 4-bits addition circuit:
- Input: we have two 4-bits binary inputs (A and B) to be added.
- Build half-adder: Use half-adder to add the least significant bits of the two input X0 and Y0. Then we use full-adder for the 3 remaining bits, considering the carry from the previous process
- Cascade Adders: Connect the outputs (sum and carry-out) of each adder to the inputs (A, B, and carry-in) of the next adder.

# III. Subtractor Operation 
## 3.1 Half subtraction
A half-subtractor circuit is used to perform a binary subtraction of two single-bit binary numbers and it has two inputs, A and B , and two outputs, DIFFERENCE and BORROW. 
## Truth table 

<img width="411" alt="image" src="https://github.com/phanreach/logic-gate/blob/main/half-subtractor2.png">

- Diff = A’B + AB’
- Borrow = A’B
## Logic circuit 

<img width="411" alt="image" src="https://github.com/Sreynaj/Binary-Mini-Calculator/assets/101303611/af4974ba-ef7c-4507-aab4-814d6432cdb9">

## 3.2 Full Subtractor
A full subtractor is a combination of circuits that performs subtraction of two bits. This circuit has three inputs and two outputs. The three inputs A, B and Bin, denote the minuend, subtrahend, and previous borrow, respectively. The two outputs, D and Bout represent the difference and output borrow.   
## Truth table:

<img width="411" alt="image" src="https://github.com/phanreach/logic-gate/blob/main/fullsubtractor.png">

## Logic circuit for full subtractor
<img width="711" alt="image" src="https://github.com/Sreynaj/Binary-Mini-Calculator/assets/101303611/bf9a0615-bb52-41df-9b3f-a5c2aa3c2f9c">






