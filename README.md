##AIM:

To perform Linear and Circular Convolution for two given sequence using SCILAB.

##APPARATUS REQUIRED:

PC installed with SCILAB.

##PROGRAM (Linear Convolution):

 clc;  
clear; 
x = [1 1 2 1]; 
 
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

##OUTPUT (Linear Convolution):

<img width="933" height="559" alt="image" src="https://github.com/user-attachments/assets/92ab4850-1843-4588-882c-1ad16944c462" />

##OUTPUT (Circular Convolution):

<img width="938" height="555" alt="image" src="https://github.com/user-attachments/assets/48bf6b6d-393a-417f-9d5f-1c1a0e06a7c1" />

##RESULT:

Linear and Circular Convolution are successfully executed in scilab
