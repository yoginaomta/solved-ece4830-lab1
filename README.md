Download Link: https://assignmentchef.com/product/solved-ece4830-lab1
<br>
Run and explain what the following Matlab program does, what are the two signals consisting of?

clear all close all sig = zeros(181,1);

i = 0:50; sig(1:51)=i; sig(52:100) = 50; sig(101:125) = 100; sig(126:130) = 0;

for i = 1:50; sig(130+i) = 50+5*randn(1); end n = 0:50; s1 = 50+5*sin(2*pi*0.1*n); s2 = 50+5*sin(2*pi*0.2*n); sig = [sig’ s1 s2]; sig = sig+50; sig(55:57) = 150; sig(59:62)=125; xx=1:283;

sign = sig+normrnd(0,5,size(sig)); % add noise

plot(xx,uint8(sign),’–‘,xx,uint8(sig),’LineWidth’,2), axis([0 283 30 170]) legend(‘noisy’,’original’)




Look at the third line from the bottom, where noise is added. If you generate 30 signals with the exact same values except for the 30 noise realizations in that part of the code, what would you do to that data to display a single signal highlighting  the transitory parts only.




Problem 2

In this part of the lab we will review the basics of sampling, in particular a sinusoid, the use of the discrete Fourier transform using the FFT command and ways to display its plot.  Keep in mind that we usually display power in dB in the frequency domain.

You are given 2500 samples taken from the AC voltage line in one of the labs at the University as shown in the Figure below. As you can see the sinusoid is not perfect.




<ul>

 <li>Knowing that this signal is of 60 Hz. Compute the sampling frequency and plot the signal in time units not sample index.</li>

 <li>Plot the signal in the frequency domain using the fft command. Plot it in real frequency with units in Hz.</li>

</ul>

A second signal is given and this time heavy equipment is on. The idea here is to identify when this equipment is on so that to start the vacuum cleaner that you see in the picture at the same time a power tool distorts the AC signal.




(c) Design an RC circuit to be connected to an electronic relay that will turn the vacuum on. Assume that the voltage signal to the relay can be amplified or attenuated to satisfy the relay specifications.




The file ACsig.mat has the two signals without and with the power tool on named x and xn respectively.




Problem 3.

Please solve the following problems from your textbook:




3.1.6       3.3.3       3.6.1

3.7.3       3.8.2       3.8.6




You can find the original problems in the next page


