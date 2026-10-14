# Project Name
Timothy Seo, Zitong Wang, Joshua Gibb
10/15/2026

- system overview/test overview
- stakeholders
- test purpose
- success criteria
- system configuration
- ground test results
- test execution
- risks


# system overview

The model rocket, which consists of the Astro 201 rocket body equipped with the Estes D12-3 rocket motor, will be launched off of Stillman Field (2160 m). The test will be split into three general phases: launch, parachute deployment, and landing. In order to record the data, the flight computer has the RP2040 Adalogger which records and stores data from the BNO085 IMU and BMP280 Barometer onto an SD card.
# stakeholders

Stakeholders in this test include Engr 201 Instructors Lt Col Firth and Col Gresham, as well as C3C Zitong Wang, C3C Timothy Seo, C3C Joshua Gibb. In addition, the School of Integrated Engineering and the Academic Wing has provided the supplies and fundings necessary to complete the test.
# test purpose

The purpose of this test is to validate the MATLAB model of the rocket, which includes its acceleration, velocity, and altitude over time. Through validating the model rocket with its MATLAB predictions, we can confidently say that the rocket meets the production criteria and is ready for further development (e.g. interceptor)
# success criteria
There are three main criteria to determine success of this test. First is accuracy of the model to the data collected from the test. In order to quantitatively measure the accuracy of the model, we will use coefficient of determination for each respective phases of the rocket. R-squared value of 0.75 or above would be considered successful. Second criteria for success 

# system configuration

The entire rocket consists of the Astro 201 rocket body, the Estes D12-3 rocket motor, an Apogee Components Parachute, and the flight controller system.
## hardware

Being the hulk of the hardware, the flight controller system is composed of a LiPo battery, Adafruit RP2040 Adalogger, BNO085 IMU, BMP280 Barometer/Pressure Sensor, and an SD card/reader. Each component serves its own purpose in allowing us to measure flight data from the rocket launch: The LiPo battery provides the power to enable other components to function, the BMP280 Barometer acts as an altimeter by measuring the pressure changes, the BNO085 IMU acts as an accelerometer, gyro, and magnetometer all in one, and the RP2040 Adalogger and its built in microSD reader allows us to record and process all the data from the other components onto an SD card.

**LiPo Battery**
- LIPO 801735 400mAh 3.7V
- Dimensions: 37.0mm x 17.5mm x 8.2mm
**Adafruit RP2040 Adalogger**
- Dimensions: 2.0" x 0.9" x 0.28"
- Mass: 6.3g
- RP2040 32-bit Cortex M0+ dual core running at ~133 MHz @ 3.3V logic and power
- 264 KB RAM
**BNO085 IMU**
- Dimensions: 1.0" x 0.9"
- Accelerometer: 3 axes of acceleration from gravity and linear motion
- Gyro: 3 axes of rotational speed
- Magnetometer: 3 axes of magnetic field sensing
- Linear acceleration vector: Three axes of linear acceleration data with the acceleration from gravity
**BMP280 Barometer**
- Dimensions: 1.0" x 0.7"
- Precision sensing solution for measuring barometric pressure with ±1 hPa absolute accuracy, temperature with ±1.0°C accuracy, and thus altitude with ±1 meter accuracy (as pressure changes with altitude).

## software

**MATLAB Version: R2025a**
- In order to create predictions and graphs for the model rocket
**VSCode**
- To run the Arduino and its components

## documentation

TRR Version 1.0

USAFA Documentation Statement: Worked with classmates to understand instructions (C2C Derek Weissinger)

# ground test results

In order to ensure accuracy in the detection of the flight phase transitions, separate ground tests of the accelerometer and barometer were conducted. For the accelerometer, a simulated launch (sharp increase in acceleration), coast, parachute, and landing phase were conducted and acceleration data was captured (Figure 6). This data is used to ensure that the On Pad -> Thrust and Thrust -> Coast phase can be captured accurately.

To test the barometer, the system was compared to a trusted barometer (Phyphox) to test the precision of the change in altitude measurements (Figure 7). The only criteria given was that an altitude change of 10 m or greater was measured, which was achieved with the 15m change in altitude. Even though the two systems measured slightly different altitudes, the change in altitude remained around the same, meaning the Arduino was relatively accurate and ready to use.

**Figure 6**
![[Acceleration_Graph.svg]]
**Figure 7**
![[altitude_plot.svg]]
# test execution
Cover the following: 
- flow—overview and point to separate procedures document
- personnel
- facilities
- resources
- documentation


# risks
Risks characterized IAW NATO S&T Flight Test Safety and Risk Management dated 2021-01: [https://apps.dtic.mil/sti/trecms/pdf/AD1183573.pdf](https://apps.dtic.mil/sti/trecms/pdf/AD1183573.pdf#page=41).
## severity

| catastrophic             | critical                      | marginal                     | negligible                    |
| ------------------------ | ----------------------------- | ---------------------------- | ----------------------------- |
| loss of life or aircraft | major damage or severe injury | minor damage or minor injury | less than minor damage/injury |
## probability

| frequent                          | probable                    | occasional                            | remote                             | improbable                              | incredible                                   |
| --------------------------------- | --------------------------- | ------------------------------------- | ---------------------------------- | --------------------------------------- | -------------------------------------------- |
| will occur often during the trial | will occur during the trial | could possibly occur during the trial | unlikely to occur during the trial | very unlikely to occur during the trial | extremely unlikely to occur during the trial |
| numerous                          | p=1                         | 1>p≥$10^{-2}$                         | $10^{-2}$>p≥$10^{-4}$              | $10^{-4}$>p≥$10^{-6}$                   | p<$10^{-6}$                                  |

## risk matrix
![](../../notes/assets/risk_matrix.png)

### risk 1: bystander injury
Errant rocket strikes and injures bystander at high speed

Risk: Medium

Mitigations
- bystanders stand at least 50 m from launch pad
- bystanders pay attention during all launch activities
- test conductor(s) call out loud countdown/launch announcements

Residual Risk: Low

|            | catastrophic | critical | marginal | negligible |
| ---------- | ------------ | -------- | -------- | ---------- |
| frequent   |              |          |          |            |
| probable   |              |          |          |            |
| occasional |              |          |          |            |
| remote     |              |          | before   |            |
| improbable |              |          | after    |            |
| incredible |              |          |          |            |

### risk 2: XXX

