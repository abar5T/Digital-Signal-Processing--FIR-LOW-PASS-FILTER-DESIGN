# Digital-Signal-Processing--FIR-LOW-PASS-FILTER-DESIGN
## AIM:
To generate design of low pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Low Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM:
```
clc; % clear screen
 clear all; % clear screen
 close all; % close all figure windows
wc=input('enter the value of cut off frequency'); 
N=input('enter the value of filter'); 
alpha=(N-1)/2; 
eps=0.001; 
%Low Pass Filter Coefficient
n=0:1:N-1; 
hd=sin(wc*(n-alpha+eps))./(pi*(n-alpha+eps))
%Bartlett Window Sequence 
n=0:1:N-1; 
wh=1-2*abs(n)/(N-1) 
hn=hd.*wh 
% Plot the Low Pass Filter with Bartlett Window Technique
w=0:0.01:pi; 
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');
```

## OUTPUT:
<img width="684" height="610" alt="image" src="https://github.com/user-attachments/assets/14baa01f-064b-48af-98cc-3128b58f4767" />


## RESULT:
<img width="1600" height="544" alt="image" src="https://github.com/user-attachments/assets/bd058f6c-b54d-4765-a329-3b72bb0e1f29" />

