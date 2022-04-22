# Lab-2-Write-Up
Valeria Rodriguez

Ziyad Gawish 

EE 157

Lab Report

# Lab 2: Getting to Know Permanent Magnet Motors

## Introduction
The back EMF is the electromotive force (voltage) that opposes the change in current that induced it. 
It is produced due to changing current in the inductor which causes a changing magnetic field around it which causes an EMF to be induced back into the motor. 
In this lab we will learn how to find and use measured constants to find the motor constant, Km. 

## Learning Objectives 
- Experimentally determine motor constants
- Analyze motor waveforms

## Materials
- bench top multimeter
- KV 1000 PM Motor
- KV 1400 PM Motor 

## Methods

## 1. KV 1000 PM Motor

### a) Electrical Frequency to Angular Velocity

To begin the experiment, the necessary motor constants were measured to correlate electrical frequency to the angular velocity: 

Given conversion between angular velocity and frequency: 

ω = 4 * pi * f/Np

f = measured frequency = 1000Hz 

Np = counted number of magnets/poles = 14 magnets/poles

ω = angular velocity = 4* pi * f/ Np = 4*pi*f/Np = 897.59791 rad/s

### b)  Measure Line-to- Line (phase-to-phase) Coil Resistance Measurement
Then, the line-to-line (LL) resistance, Rl, was measured to be about 0.4 ohms using a benchtop multimeter. 
Then the contact resistance of the probes was measured by reading the resistance when the probes are shorted together, 01. ohm, and subtracted from the LL resistance measurement for a final LL resistance value of 0.3 ohms. 

Contact Resistance from probes (DMM)  = 0.1 ohm

Measured resistance = 0.4 ohm

RLL =(Measured R - Contact R) = (0.4 - 0.1) = 0.3 ohm

Rcoil = 0.3/2 = 0.15 ohms


### c) Back EMF Measurement
The back EMF was measured by spinning the motor up under power, cutting the and then capturing the back EMF as the motor spins down with the ESC off, yielding an EMF waveform. 
This procedure was done to capture the back EMF of both the KV 1000 and KV 4000 PM motors at different speeds. 

Measured Vpp (Voltage peak-to-peak) using scope: Vpp = ~8.8V

Vamp  = 4.4V  

VLL = 4.4V

Vemf = VLL - I*RLL = (4.4V - 0) = 4.4V

Kb = VLL / omega = 0.0049019722

![m11emf](https://user-images.githubusercontent.com/71746051/164656858-2611fbed-855c-479f-a0d7-71a7cbfa631c.png)


### d) Km and Characterizing Drag Torque (Hysteresis and Eddy Current) 
- Find Kt from Kb knowing the following:

Ktau = Kb

Ktau avg = Ktau/sqrt Ploss/Rcoil 

Km = Ktau avg/sqrt Ploss

Km = t avg/sqrt Ploss

Km = Kt/squ of Rcoil 

Km = Kb/sqrt 1/Rcoil =  (0.0049019722/sqrt 1/1.5) = .0126568379

- Phase to Phase Voltage and Calculated Back EMF

![bemfmotor1](https://user-images.githubusercontent.com/71746051/164649083-9d7eec03-2cbc-4028-ab4c-91a5ebc6190f.png)


- Measured Phase Current and Phases

![m1pc](https://user-images.githubusercontent.com/71746051/164662959-cc6f73a5-eb87-48f5-be9f-beeae7b3ae29.png)


- Phases

![m1ppp](https://user-images.githubusercontent.com/71746051/164664858-358319d6-49c9-422c-a590-6d5c1921321c.png)


- Instantaneous Torque from Single Phase

![m1ittt](https://user-images.githubusercontent.com/71746051/164665903-293b4c75-35f7-4c2d-bfaf-d2400145a639.png)


- Loss Torque Plot (Eddy Current Torque + Hysteresis Torque) and as Power Relationship

Total torque = torque avg * 3 = 0.001501852333852542

Thereofore, the total torque at 718 rad/sec for motor 1: 0.001501852333852542


![m1edt](https://user-images.githubusercontent.com/71746051/164648699-5c169d57-23ce-4265-8869-e1fd819d7a03.png)

![m1pt](https://user-images.githubusercontent.com/71746051/164648713-19d159c4-ab8c-4300-96cf-97d6b62609c2.png)



## 2. KV 1400 PM Motor

### a) Electrical Frequency to Angular Velocity

f = measured frequency = 714.285714 Hz 

Np = counted number of magnets/poles = 14 magnets/poles

ω = angular velocity = 4 * pi * f/ Np = 641 rad/s


### b)  Measure Line-to- Line (phase-to-phase) Coil Resistance Measurement

Contact Resistance from probes (DMM)  = 0.1 ohm

Measured resistance = 0.4 ohm

RLL = (Measured R - Contact R) = (0.4 - 0.1) = 0.3 ohm

Rcoil = 0.3/2 = 0.15 ohms


### c) Back EMF Measurement

Measured Vpp (Voltage peak-to-peak) using scope: Vpp = ~8V

Vamp  = 4V  

VLL = 4V

Vemf = VLL - I*RLL = (4V - 0) = 4V

Kb = VLL / omega = 0.006239


![m2emfrrrr](https://user-images.githubusercontent.com/71746051/164670076-c2ba61e0-3165-4770-876b-ac1177619a81.png)



### d) Km and Characterizing Drag Torque (Hysteresis and Eddy Current) 
- Find Kt from Kb knowing the following:

Ktau = Kb

Ktau avg = Ktau/sqrt Ploss/Rcoil 

Km = Ktau avg/sqrt Ploss

Km = t avg/sqrt Ploss

Km = Kt/squ of Rcoil 

Km = Kb/sqrt 1/Rcoil =  (0.0049019722/sqrt 1/1.5) = .0161090287


- Phase to Phase Voltage and Calculated Back EMF

![m2emf](https://user-images.githubusercontent.com/71746051/164651312-d0961d64-25c0-4ffc-8c9c-26b780a9db13.png)


- Measured Phase Current and Phases


![m2cccccc](https://user-images.githubusercontent.com/71746051/164673523-66a3887e-a177-4e8c-8ca7-a17a049197b5.png)


- Phases

![m2ppppp](https://user-images.githubusercontent.com/71746051/164673059-aad06883-5fb1-4981-9929-ad8c9ad5acec.png)


- Instantaneous Torque from Single Phase

(Typo in titles meant to display Motor 2)

![m2itttttt](https://user-images.githubusercontent.com/71746051/164673611-41dcde94-9fa8-4c95-bf98-6c008170d881.png)


- Loss Torque Plot (Eddy Current Torque + Hysteresis Torque) and as Power Relationship

Total torque = torque avg * 3 = 0.002919432420947719

Thereofore, total Torque at 390 rad/sec for motor 2: 0.002919432420947719

(Typo in titles meant to display Motor 2)


![m2dt](https://user-images.githubusercontent.com/71746051/164651537-dfad6757-3eb8-4e90-bf1b-ac915b5fe2d2.png)


![m2dp](https://user-images.githubusercontent.com/71746051/164651776-bee5ad23-877b-428d-8c77-be26d40cdf41.png)










