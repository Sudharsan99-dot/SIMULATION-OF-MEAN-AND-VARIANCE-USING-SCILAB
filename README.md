# SIMULATION-OF-MEAN-AND-VARIANCE-USING-SCILAB
# AIM:
To write a program for mean, variance and cross correlation in SCILAB and verify the output.

# EQUIPMENTS Needed
• Computer with i3 Processor • SCI LAB

# Algorithm
1. Define the Function: Specify the function you want to simulate. For example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
2. Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
3. Evaluate the Function: Compute the function values at each of these sample points.
4. Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
5. Display Results: Output the computed mean variance and Cross Correlation PROCEDURE • Refer Algorithms and write code for the experiment. • Open SCILAB in System • Type your code in New Editor • Save the file • Execute the code • If any Error, correct it in code and execute again • Verify the generated results
# PROGRAM
```scilab
clear;
clc;
clear;

function X=f(x)
    z=2*(1-x)^2,
    X=x*z
endfunction
a=0;
b=1;
EX=intg(a,b,f);

function Y=c(y)
    z=2*(1-y)^2,
    Y=y*z
endfunction
EY=intg(a,b,c);

disp(EX,"i)Mean of X =")
disp(EY,"Mean of Y=")

function X=g(x)
    z=2*(1-x)^2, 
    X=x^2*z,
endfunction
a=0;
b=1;
EX2=intg(a,b,g);
 
function Y=h(y)
    z=2*(1-y)^2, 
    Y=y^2*z'
endfunction 
EY2=intg(a,b,h);

vX2=EX2-(EX)^2;
vY2=EY2-(EY)^2;

disp(vX2,"ii)Variance of X"); 
disp(vY2,"Variance of Y");

x= input("type in the reference sequence="); 
y= input("type in the second sequence="); 
n1=max(size(y))-1;
n2=max(size(x))-1;
r=corr(x,y,n1);
plot2d3('gnn',r);
```
# OUTPUT

<img width="505" height="735 alt="result" src="https://github.com/user-attachments/assets/4f33dd9e-a489-4b46-9068-79006a8f7db3" />

<img width="610" height="460" alt="image" src="https://github.com/user-attachments/assets/8292014a-f835-4661-b71e-f25e59d63492" />

# CALCULATIO

![1](https://github.com/user-attachments/assets/663591b3-391b-4913-8ed7-d921eb5cea12)
![2](https://github.com/user-attachments/assets/49cc9acb-d63d-4691-8eb7-84a5c4ade636)
![3](https://github.com/user-attachments/assets/367c5e1d-4117-4748-ad5b-942cedc56a4c)

# RESULT:
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.
