# EXP NO: 4 GENERATION AND DETECTION OF FM

### Aim:

To generate and detect the Phase modulation and  using S C I L A B.

### Equiptments Required:

• Computer with i3 Processor

• SCI LAB

### Theory:

Frequency modulation is a type of modulation in which the frequency of the high frequency (carrier) is varied in accordance with the instantaneous value of the modulating signal. FREQUENCY DEVIATION f and MODULATION INDEX m f : The frequency deviation f represents the maximum shift between the modulatedsignal frequency, over and under the frequency of the carrier.

We define modulation index m f the ratio between f and the modulating frequency m= f / fm

### Frequency Modulation Generation: 
Phase Modulation (PM) is a technique where the phase of the carrier wave is varied in proportion to the instantaneous amplitude of the input signal (message signal). Unlike frequency modulation, where the frequency is varied, in phase modulation, the phase angle of the carrier wave changes with the amplitude of the message signal.

The general form of a PM signal can be represented as:

<img width="485" height="273" alt="image" src="https://github.com/user-attachments/assets/4aad9c4d-d225-4c2a-8a18-7c1539676e39" />

### Algorithm:

#### 1.Initialize Parameters:
  • Set values for carrier amplitude (AcA_cAc), carrier frequency (fcf_cfc), message frequency (fmf_mfm), sampling frequency, and phase deviation sensitivity (kpk_pkp).
#### 2.Generate Time Axis:
  • Create a time vector for the signal duration based on the sampling frequency.
#### 3.Generate Message Signal:
  • Define the message signal as a cosine wave.
#### 4.Generate PM Signal:
  • Apply the PM modulation formula to obtain the modulated signal.
#### 5.Plot the Signals:
  • Use Matplotlib to plot the message signal, carrier signal, and phase-modulated signal.

### Procedure:

• Refer Algorithms and write code for the experiment. 

• Open SCILAB in System.

• Type your code in New Editor. 

• Save the file.

• Execute the code.

• If any Error, correct it in code and execute again.

### Model Graph:

<img width="410" height="293" alt="image" src="https://github.com/user-attachments/assets/523128c9-f936-43d0-b7fb-04a2bcaf7efb" />

### Program:
~~~
Am=12.33;
Ac=19.728;
fm=1034;
fc=10340;
fs=1034000;
t=0:1/fs:2/fm;
b=3.73;
em=Am*cos(2*3.14*fm*t);
subplot(4,1,1);
plot(t,em);
ec=Ac*cos(2*3.14*fc*t);
subplot(4,1,2);
plot(t,ec);
efm=Ac*cos(2*3.14*fc*t+b*sin(2*3.14*fm*t));
subplot(4,1,3);
plot(t,efm);
epm=Ac*cos(2*3.14*fc*t+b*cos(2*3.14*fm*t));
subplot(4,1,4);
plot(t,epm);
~~~
### Output Waveform:

<img width="1419" height="1259" alt="image" src="https://github.com/user-attachments/assets/439648ce-c20b-4919-a8e0-bf4bb2242901" />

### Result:
The message signal, carrier signal, and phase-modulated (PM) signal will be displayed in separate plots. The modulated signal will show phase variations corresponding to the amplitude of the message signal.
