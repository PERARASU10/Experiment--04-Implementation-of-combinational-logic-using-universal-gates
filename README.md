# Experiment--04-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
 
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

## Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram

Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram
## Procedure

1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.

## Program:

Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
Developed by: PERARASU M        
RegisterNumber:  22008454        

using NAND:

   module combo1(a,b,c,d,f);   
   
   input a,b,c,d;      
   
   output f;     
   
   wire p,q,r;     
   
   assign p=(~c & b & a);    
   
   assign q=(~d & c & ~a);    
   
   assign r=(c & ~b & a);   
   
   assign f=(~(~p & ~q & ~r));  
   
   endmodule      

using NOR:

   module combo2(a,b,c,d,f);      
   
   input a,b,c,d;       
   
   output f;   
   
   wire p,q,r;  
   
   assign p=( c & ~b & a); 
   
   assign q=( d & ~c & a);
   
   assign r=( c & ~b & a);
   
   assign f=(~(~( p | q | r)));
   
   endmodule

## RTL realization

## Output:
USING NAND GATE :

RTL

![USING NAND RTL](https://user-images.githubusercontent.com/118348589/211006636-101f2666-d279-47e8-8b87-a239d592212b.png)

TIMING DIAGRAM

![USING NAND GATE TIMING DIAGRAM](https://user-images.githubusercontent.com/118348589/211006807-eac3d4ff-aafa-4361-87c1-4a615515df3f.png)

TRUTH TABLE 

![USING NAND GATE TRUTH TABLE](https://user-images.githubusercontent.com/118348589/211006860-84cb5096-3566-4112-8d82-8f705a49d27f.png)

USING NOR GATE :   

RTL

![USING NOR RTL](https://user-images.githubusercontent.com/118348589/211007138-d56d38c6-6c3b-4e10-80c6-33a15000ab90.png)

TIMING DIAGRAM

![USING NOR TIMING DIAGRAM](https://user-images.githubusercontent.com/118348589/211007189-b1181634-734b-4a44-b98d-7c84668ab88c.png)

TRUTH TABLE

![USING NOR TRUTH TABLE](https://user-images.githubusercontent.com/118348589/211007243-a6bc725f-48ca-412c-a4f0-3d238deab603.png)

## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
