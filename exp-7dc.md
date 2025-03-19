## EX-Phase Shift Keying (PSK)
## LOKESH KUMAR.B_212223060139
## write a  Phase Shift Keying (PSK) Modulation in Python
## AIM
To perform Phase Shift Keying (PSK) Modulation in Python
## APPARATUS REQUIRED:
  Python 3.x
## PROGRAM
```
import numpy as np
import matplotlib.pyplot as plt

# Generate random binary data (0s and 1s)
data = np.random.randint(0, 2, 10)
print("Input Data:", data)

# BPSK Modulation: Mapping 0 -> -1 and 1 -> +1
bpsk_signal = 2 * data - 1

# Create time axis
t = np.linspace(0, 1, 100)

# Carrier Wave (Cosine)
carrier = np.cos(2 * np.pi * 5 * t)

# Modulated Signal
modulated_signal = np.array([bit * carrier for bit in bpsk_signal]).flatten()

# Time axis for plotting
time_axis = np.linspace(0, len(data), len(modulated_signal))

# Plotting the results
plt.figure(figsize=(10, 6))

plt.subplot(3, 1, 1)
plt.stem(data, use_line_collection=True)
plt.title("Input Binary Data (0s and 1s)")
plt.xlabel("Bit Index")
plt.ylabel("Bit Value")

plt.subplot(3, 1, 2)
plt.plot(time_axis, modulated_signal)
plt.title("BPSK Modulated Signal")
plt.xlabel("Time")
plt.ylabel("Amplitude")

plt.subplot(3, 1, 3)
plt.plot(t, carrier)
plt.title("Carrier Wave (Cosine)")
plt.xlabel("Time")
plt.ylabel("Amplitude")

plt.tight_layout()
plt.show()

```
## PROGRAM WAVEFRONT
![Screenshot 2025-03-19 144419](https://github.com/user-attachments/assets/17a6b1d7-8411-4d0c-9ca2-b31246f09a6d)





## RESULT
  THUS THE Phase Shift Keying (PSK) Modulation IS PERFORMED USING PHYTON
