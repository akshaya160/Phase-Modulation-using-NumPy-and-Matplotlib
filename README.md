# Phase-Modulation-using-NumPy-and-Matplotlib

### Aim
To implement and analyze phase modulation (PM) using Python's NumPy and Matplotlib libraries.   
### Apparatus Required
1.	Software: Python with NumPy and Matplotlib libraries  
2.	Hardware: Personal Computer Theory  
Phase Modulation (PM) is a technique where the phase of the carrier wave is varied in proportion to the instantaneous amplitude of the input signal (message signal). Unlike frequency modulation, where the frequency is varied, in phase modulation, the phase angle of the carrier wave changes with the amplitude of the message signal.  

The general form of a PM signal can be represented as:


<img width="306" height="241" alt="image" src="https://github.com/user-attachments/assets/b8d2db63-afe0-4bd8-8826-efc89a111423" />

### Algorithm

1.	Initialize Parameters:  
o	Set values for carrier amplitude (AcA_cAc), carrier frequency (fcf_cfc), message frequency (fmf_mfm), sampling frequency, and phase deviation sensitivity (kpk_pkp).  
2.	Generate Time Axis:  
o	Create a time vector for the signal duration based on the sampling frequency.  
3.	Generate Message Signal:  
o	Define the message signal as a cosine wave.  
4.	Generate PM Signal:  
o	Apply the PM modulation formula to obtain the modulated signal.  
5.	Plot the Signals:   
o	Use Matplotlib to plot the message signal, carrier signal, and phase-modulated signal.  


### Program
```
Am = 3.2;
Ac=6.4;
fm = 154;
fc=1540;
fs = 15400;
B = 3.3;
t = 0:1/fs:2/fm;
em = Am*cos(2*3.14*fm*t);
subplot(4,1,1);
plot(t,em);
ec = Ac*cos(2*3.14*fc*t);
subplot(4,1,2);
plot(t,ec);
eFM = Ac*cos((2*3.14*fc*t) + (B*sin(2*3.14*fm*t)));
subplot(4,1,3);
plot(t,eFM);
ePM = Ac*cos((2*3.14*fc*t) + (B*cos(2*3.14*fm*t)));
subplot(4,1,4);
plot(t,ePM);


### Tabulation
```
<img width="627" height="907" alt="image" src="https://github.com/user-attachments/assets/f161639f-8bbf-46c9-8b1a-65572460416b" />

### Output

![WhatsApp Image 2026-03-31 at 12 31 41 PM](https://github.com/user-attachments/assets/b06479ba-dda7-4e11-9d6d-c94ac647e238)



### Result

Thus the Phase-Modulation  are executed in Scilab and output is verified.

