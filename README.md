### EXPT 2a: LINEAR CONVOLUTION-USING-DFT
### AIM
To perform and verify linear convolution operation of two given sequences using SCILAB.

### APPARATUS REQUIRED
PC installed with SCILAB

### PROGRAM:
```
clc;
clear;
x = [1 1 1 1];
h = [1 2 3 4];
m = length(x);
n = length(h);
a=0:1:m-1;
b=0:1:n-1;
subplot(3,1,1);
plot2d3(a,x);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Input Signal X');
subplot(3,1,2);
plot2d3(b,h);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Impulse Signal h');
for i = 1: n+m-1
conv_sum = 0;
for j = 1:i
if (((i-j+1) <= n)&(j <=m))
conv_sum = conv_sum + x(j)*h(i-j+1);
end;
y(i) = conv_sum;
end;
end;
disp(y,'Convolution Sum using Direct Formula Method = ')
subplot(3,1,3);
plot2d3(y)
title('Graphical Representation of output Signal y');
```

### CALCULATIONS:

<img width="628" height="1110" alt="image" src="https://github.com/user-attachments/assets/b685bbea-6095-4703-bbd6-6eb6d55e0bd6" />

<img width="1280" height="803" alt="image" src="https://github.com/user-attachments/assets/edaaf6de-922d-4b90-b152-065a9516967f" />



### SAMPLE OUTPUT:


<img width="1920" height="1020" alt="Screenshot 2026-07-28 093439" src="https://github.com/user-attachments/assets/9926cb87-8f6c-4416-845d-5a6dc5f383ed" />





RESULT:
Thus, the linear convolution of the two given sequences were performed and its result was verified.
