# Digital-Signal-Processing--Correlation
## AIM:
To generate discrete auto correlation and cross correlation of signals using MATLAB.
## APPARATUS REQUIRED:
MATLAB R2012.
## ALGORITHM:
Step 1: Open matlab. Write the program.

Step 2: Read the input sequence 1 and input sequence 2 sequence.

Step 3: Perform auto correlation and cross correlation for both the sequences. 

Step 4: Plot the output sequence with x-label and y-label with suitable title.

Step 5: Terminate the program.


## PROGRAM: 
```
clc;
clear;
close all;

%% INPUT SIGNAL 1
x = input('Enter the x(n) sequence: ');
n = 0 : length(x) - 1;

figure(1);
stem(n, x);
xlabel('Time');
ylabel('Amplitude');
title('Input Signal 1');

%% INPUT SIGNAL 2
h = input('Enter the h(n) sequence: ');
m = 0 : length(h) - 1;

figure(2);
stem(m, h);
xlabel('Time');
ylabel('Amplitude');
title('Input Signal 2');

%% DISCRETE AUTO CORRELATION
auto_corr = xcorr(x, x);
n1 = -(length(x)-1) : (length(x)-1);

figure(3);
stem(n1, auto_corr);
xlabel('Time');
ylabel('Amplitude');
title('Discrete Auto Correlation Waveform');

%% DISCRETE CROSS CORRELATION
cross_corr = xcorr(x, h);
n2 = -(length(h)-1) : (length(x)-1);

figure(4);
stem(n2, cross_corr);
xlabel('Time');
ylabel('Amplitude');
title('Discrete Cross Correlation Waveform');
```

## OUTPUT:
![WhatsApp Image 2026-04-09 at 10 20 46](https://github.com/user-attachments/assets/8ed349b7-7837-4d03-ad5e-36178d03a38a)


## RESULT:
![WhatsApp Image 2026-04-09 at 10 18 05](https://github.com/user-attachments/assets/ecfb1a31-f3a4-462d-bf3c-91f6627114ae)


