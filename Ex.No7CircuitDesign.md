# Ex.No: 7  Logic Programming –  Logic Circuit Design
### DATE:01-04-2024                                                                  
### REGISTER NUMBER : 212221040105
### AIM: 
To write a logic program to design a circuit like half adder and half subtractor.
###  Algorithm:
1. Start the Program
2. Design a AND gate logic if both inputs are 1 then output is 1.
3. Design a OR gate logic if any one of input is 1 then output is 1.
4. Design a XOR gate logic if both inputs are different then output is 1.
5. Design a NOT gate logic if input is 0 then output is 1.
6. Design a half adder and half subtractor using the rules.
7. Test the logic.
8. Stop the program.

### Program:
```
xor(0,1,1).
xor(0,0,0).
xor(1,0,1).
xor(1,1,0).
and(1,1,1).
and(0,0,0).
and(0,1,0).
and(1,0,0).
not(0,1).
not(1,0).
or(0,1,1).
or(1,0,1).
or(0,0,0).
or(1,1,1).
halfadder(A,B,Sum,Carry):-
    xor(A,B,Sum),
    and(A,B,Carry).
halfsubtractor(A,B,Diff,Carry):-
    xor(A,B,Diff),
    not(A,C),
    and(C,B,Carry).
fulladder(A,B,Cin,S,Cout):-
    xor(A,B,X),
    xor(X,Cin,S),
    and(X,Cin,Y),
    and(A,B,Z),
    or(Y,Z,Cout).
```
### Output:
![WhatsApp Image 2024-04-01 at 15 38 07_8829e1da](https://github.com/mehanthyka/AI_Lab_2023-24/assets/127507580/05528514-759a-4830-8a31-58dd24c7369f)
![WhatsApp Image 2024-04-01 at 15 40 48_c272919a](https://github.com/mehanthyka/AI_Lab_2023-24/assets/127507580/71f61364-e4ff-4b3a-b02d-02472cca661d)
![WhatsApp Image 2024-04-01 at 15 40 52_2bddf4b2](https://github.com/mehanthyka/AI_Lab_2023-24/assets/127507580/0b7e7001-4dfe-4755-8fa7-9e6b8d501ecc)

### Result:
Thus the truth table of circuit verified sucessfully.
