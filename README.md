## Developed by: TARUNIKA.D
## RegisterNumber:  23000559
## Exp-02-Implementation of Half Adder and Full Adder circuit:

### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.


### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
# Theory
Adders are digital circuits that carry out addition of numbers.
 
### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.
Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)
#### Figure -01 HALF ADDER 
### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.




## Program:
module project_3(sum, carry,a,b);

input a,b;

output sum, carry;

xor sum1 (sum, a,b);

and carry1 (carry,a,b);

endmodule



### RTL realisation
![Screenshot 2023-12-11 132442](https://github.com/mounika2005/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145633112/71b0c991-2017-4faf-bfd6-3ca3991e59ae)
### timing diagram 
![Screenshot 2023-12-11 132553](https://github.com/mounika2005/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145633112/2cb33219-c37a-4f0a-bae7-96da5250f569)
### truth table
![Screenshot 2023-12-11 132628](https://github.com/mounika2005/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145633112/7f987f89-e401-41bd-8055-62d61a6f286f)

#### 02 FULL ADDER 
### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A'B'Cin + A'BCin' + ABCin + AB'Cin' = AB Cin Carry = AB+ ACin + BCin
![Screenshot 2023-12-11 132703](https://github.com/mounika2005/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145633112/f785da90-4b4c-46b7-aa09-20e4ba8b692d)

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
## program
module project_3_2(a, b, c, sum, carry);

input a,b,c;

output sum, carry;

xor (sum, a,b,c);

assign carry=a&b | b&c | a&c;

endmodule
## RTL realisation 
![Screenshot 2023-12-11 133102](https://github.com/mounika2005/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145633112/66f79611-1be5-43dc-aada-df1fd5a68375)

### TIMING DIAGRAM
![Screenshot 2023-12-11 133137](https://github.com/mounika2005/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145633112/89e545f0-d4e8-4a0e-ba11-c219dfe1f5d6)
### TRUTH TABLE 
![Screenshot 2023-12-11 133144](https://github.com/mounika2005/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145633112/e6e598de-4aa8-45a7-b964-fbe56acc9376)

### Result:

Thus the given logic functions are implemented and their operations are verified using verilog programming.
