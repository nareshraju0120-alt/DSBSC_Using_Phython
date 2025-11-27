# DSBSC_Using_Python


Aim


To implement and analyze DSBSC modulation and demodulation  using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Double Sideband Suppressed Carrier (DSBSC) modulation is a type of amplitude modulation in which the carrier signal is suppressed, and only the two sidebands containing the information are transmitted. In DSBSC, the transmitted signal consists of the upper sideband (USB) and the lower sideband (LSB) components, which carry the same information as the carrier but without wasting power on the carrier itself.


Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate DSBSC Signal: Apply the DSBSC modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signals.

Program
```
import numpy as np
import matplotlib.pyplot as plt

Am = 6
fm = 504
Ac = 12
fc = 5040
fs = 50400

t = np.arange(0, 0.01, 1/fs)

message = Am * np.cos(2 * np.pi * fm * t)
carrier = Ac * np.cos(2 * np.pi * fc * t)
dsbsc = message * carrier

plt.figure(figsize=(10, 6))

plt.subplot(3, 1, 1)
plt.plot(t, message)

plt.subplot(3, 1, 2)
plt.plot(t, carrier)

plt.subplot(3, 1, 3)
plt.plot(t, dsbsc)

plt.tight_layout()
plt.show()

```

Output Waveform

<img width="1189" height="790" alt="image" src="https://github.com/user-attachments/assets/836598e8-aad7-4877-b204-a5a7adb141a7" />

Tabular Column

<img width="1269" height="950" alt="image" src="https://github.com/user-attachments/assets/34baf9ff-705c-426e-a0a7-50b89ef22e0e" />

Result


Thus the DSB-SC-AM Modulation and Demodulation is generated.
