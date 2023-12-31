## Name: Siranjeevi.S
## Ref.no: 23012822

# Experiment--04-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure
## A. Half Subtractor:

1. A half subtractor is a combinational circuit that performs the subtraction of two single-bit numbers and produces two outputs: the difference and the borrow.

2. Let's consider two single-bit inputs A and B.

3. Difference (Diff): This output represents the result of the subtraction A - B and is obtained by performing an XOR operation on inputs A and B.

4. Borrow (Borrow): This output indicates whether a borrow is required for the subtraction and is obtained by performing an AND operation between the complement of A and B.

## B. Full Subtractor:

1. A full subtractor is a combinational circuit that subtracts three single-bit inputs: A, B, and a Borrow-In (Bin), and produces two outputs: the difference and a Borrow-Out (Bout) to the next subtractor in a sequence.

2. Difference (Diff): This output represents the result of the subtraction A - B -Bin.

3. Borrow-Out (Bout): This output indicates whether a borrow is required for the subtraction and will be used in further subtractors.

4. A full subtractor is typically constructed using two half subtractors. The Borrow-Out of the first half subtractor is used as an input Borrow-In for the second half subtractor. The outputs of the half subtractors are combined to generate the final Difference and Borrow-Out.





## Program:
![Screenshot 2023-12-31 074426](https://github.com/vasanthkumarch/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152168132/62892089-211c-4477-8264-a2feaf9b2424)

##  RTL realization:
![Screenshot 2023-12-31 074500](https://github.com/vasanthkumarch/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152168132/4947fcae-3ab6-4fa2-8ed4-81f38d3df466)


![Screenshot 2023-12-31 074526](https://github.com/vasanthkumarch/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152168132/f1fd097e-8ec2-487d-8863-b1e7611d1762)



## Truth tabel:
![Screenshot 2023-12-31 074554](https://github.com/vasanthkumarch/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152168132/c813f47e-2c12-4be8-8380-1b4eda30d3f8)



## Timing diagram :
![Screenshot 2023-12-31 074618](https://github.com/vasanthkumarch/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152168132/68935e59-68ae-48ae-bc8b-c0b90074f9e4)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
