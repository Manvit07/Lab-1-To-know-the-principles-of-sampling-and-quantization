# Lab-1-To-know-the-principles-of-sampling-and-quantization

close all;
clc;
t=0:0.001:1;
fm=10;
am=1;
x=am*sin(2*pi*fm*t);
subplot(2,2,1);
plot(t,x,'LineWidth',2)
xlabel('time')
ylabel('amplitude')
grid;
title('Message input signal');
n1=-5:1:5;
fs1=1.6*fm;
fs2=2*fm;
fs3=8*fm;
x1=am*cos(2*pi*fm/fs1*n1);
subplot(2,2,2);
stem(n1,x1,'LineWidth',3)
xlabel('Number of samples')
ylabel('amplitude')
grid;
title('under sampling');
n2=-5:1:5;
x2=cos(2*pi*fm/fs2*n1);
subplot(2,2,3);
stem(n2,x2,'LineWidth',3)
xlabel('Number of samples')
ylabel('amplitude')
hold on;
title('uniform sampling');
n3=-20:1:20;
x3=cos(2*pi*fm/fs3*n3);
subplot(2,2,4);
stem(n3,x3,'LineWidth',3)
hold on;
xlabel('Number of samples')
ylabel('amplitude')
gri;
title('over sampling');
