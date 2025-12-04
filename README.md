# FM-using-Python

Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program
import numpy as np
import matplotlib.pyplot as plt
Am=5.5
fm=441
Ac=11.0
fc=4410
fs=44100
b=5.6
t=np.arange(0,2/fm,1/fs)
m=Am*np.cos(2*np.pi*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c=Ac*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
s=Ac*np.cos((2*np.pi*fc*t)+(b*np.sin(2*np.pi*fm*t)))
plt.subplot(3,1,3)
plt.plot(t,s)

Output Waveform
<img width="554" height="413" alt="image" src="https://github.com/user-attachments/assets/a2cab6a7-69cc-4ba8-8469-fc439fc1262f" />

Tabular Column

<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/ddf76d7d-bbcf-4ec4-9d42-a87d77d2e918" />


Calculation




Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
