# Experiment--02-Implementation-of-combinational-logic

## AIM:
To implement the given logic function and verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
### Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime

## Program:
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.

Developed by: NATHIN R

RegisterNumber:  212222230090
*/
```
module Verilog1(a,b,c,d,w,x,y,z,F1,F2);
input a,b,c,d,w,x,y,z;
output F1,F2;
wire  A1,A2,A3,A4,A5,B1,B2,B3,B4,B5;
assign A1= (~a&(~b)&(~c)&(~d));
assign A2= (a&c&(~d));
assign A3= ((~b)&c&(~d));
assign A4= (~a&b&c&d);
assign A5= (b&(~c)&d);
assign F1= A1|A2|A3|A4|A5;
assign B1= (x&(~y)&z);
assign B2= (~x&(~y)&z);
assign B3= (~w&x&y);
assign B4= (w&(~x)&y);
assign B5= (w&y&z);
assign F2= B1|B2|B3|B4|B5;
endmodule		 
```
## Output:
## RTL
![image](https://user-images.githubusercontent.com/118679646/233277589-5333b9b5-8a9f-4cac-a443-dc10e6315820.png)

## Timing Diagram
![image](https://user-images.githubusercontent.com/118679646/233277425-6d60de16-02b9-4934-be5a-f489660c9ab4.png)

## Truth Table:
![WhatsApp Image 2023-04-27 at 10 50 53](https://user-images.githubusercontent.com/118679646/234766472-e09546ea-fffe-408a-8e5d-0a87a90bdeee.jpg)

## Result:
Thus the given logic functions are implemented using  logic gates.
