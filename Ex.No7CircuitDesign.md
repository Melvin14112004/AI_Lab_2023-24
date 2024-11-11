# Ex.No: 7  Logic Programming –  Logic Circuit Design
### DATE: 12.9.24                                                                           
### REGISTER NUMBER : 212222040098
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
```py
and(0,0,0).
and(0,1,0).
and(1,1,1).
and(1,0,0).
xor(1,0,1).
xor(1,1,0).
xor(0,1,1).
xor(0,0,0).
not(0,1).
not(1,0).
or(0,0,0).
or(0,1,1).
or(1,1,1).
or(1,0,1).
halfadder(A,B,Sum,Carry):-
    xor(A,B,Sum),
    and(A,B,Carry).
halfsubtractor(A, B, Difference, Borrow):-
    xor(A, B, Difference),
    not(A, NA),
    and(NA, B, Borrow).
fulladder(A, B, Cin, Sum, Cout) :-
    xor(A, B, Xor1),
    xor(Xor1, Cin, Sum),
    and(A, B, And1),
    and(Xor1, Cin, And2),
    or(And1, And2, Cout).
full_subtractor(A, B, Bin, Difference, Bout) :-
    xor(A, B, Xor1),
    xor(Xor1, Bin, Difference),
    not(A, NotA),      % Apply NOT to A first
    and(NotA, B, And1),
    and(Xor1, Bin, And2),
    or(And1, And2, Bout).
```

### Output:

![Screenshot 2024-09-23 214814](https://github.com/user-attachments/assets/384df012-29d6-49d9-959c-53f559114344)


### Result:
Thus the truth table of circuit verified sucessfully.
