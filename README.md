# DSBSC


EX NO: 2	DSB-SC-AM MODULATOR AND DEMODULATOR

AIM:

To write a program to perform DSBSC modulation and demodulation using SCI LAB and study its spectral characteristics

EQUIPMENTS REQUIRED

•	Computer with i3 Processor
•	SCI LAB

Note: Keep all the switch faults in off position

Algorithm:

1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the message signal.
•	Amplitude: Maximum amplitude of the message signal.
2.	Generate Signals:
•	Message Signal: A sinusoidal signal that will be modulated.
•	Carrier Signal: A high-frequency sinusoidal signal used for modulation.
3.	DSBSC Modulation:
•	Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal.
4.	DSBSC Demodulation:
•	Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components).
•	Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal.
5.	Visualization:
Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation.



PROCEDURE

•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
 
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated waveform using Tabulation and Model Waveform



Model Waveform




<img width="703" height="679" alt="image" src="https://github.com/user-attachments/assets/e7c7c7f8-ccf2-41ac-b1f3-325989941a6f" />




Program



Am = 6.2;

fm = 474;

Ac = 12.4;

fc = 4740;

fs = 47400;

t = 0:1/fs:3/fm;

m = Am*cos(2*3.14*fm*t);

subplot(3,1,1);

plot(t,m);

title('Message Signal');

c = Ac*cos(2*3.14*fc*t);

subplot(3,1,2);

plot(t,c);

title('Carrier Signal');

s1=(Ac+m).* cos(2*3.14*fc*t);

s2=(Ac-m).* cos(2*3.14*fc*t);

s = s1-s2;

subplot(3,1,3);

plot(t,s);

title('DSBSC Modulated Signal');






Output Graph



<img width="610" height="460" alt="image" src="https://github.com/user-attachments/assets/1a250787-554a-4ca6-8fd2-b9c2c9554e35" />





Tablular Column



![WhatsApp Image 2025-09-28 at 22 50 09 (1)](https://github.com/user-attachments/assets/46d916d2-ced9-47ea-af92-ea5f3fd9c6f7)






Result

Thus the DSB-SC-AM Modulation and Demodulation is generated.

