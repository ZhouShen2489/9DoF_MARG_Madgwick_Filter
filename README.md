# MPU9250 Madgwick Filter Attitude Estimation
## Description
This project inplements attitude estimation by using [Madgwick filter](https://x-io.co.uk/open-source-imu-and-ahrs-algorithms/), which is a low computational cost and high accuracy data fusion algorithm, based on a 9 degree of freedom MARG(magnetic angular rate and gravity, i.e., IMU + magnetometer). The MARG used in this project is [MPU9250](https://www.amazon.com/HiLetgo-Gyroscope-Acceleration-Accelerator-Magnetometer/dp/B01I1J0Z7Y/ref=sr_1_4?dchild=1&keywords=MPU9250&qid=1597109421&sr=8-4), [MPU9255](https://www.amazon.com/UCTRONICS-MPU-9255-Compass-Accelerometer-Gyroscope/dp/B01DIGRR8U/ref=sr_1_3?dchild=1&keywords=MPU9255&qid=1597109290&sr=8-3) is also supported since they use same library in Arduino. A [Teensy4.0](https://www.pjrc.com/teensy-4-0/) is used to receive and process the data from MPU9255, then send results of attitude estimation as Euler angle to PC.

**To view the performance, please click [here](https://youtu.be/iOwcov_5z3c).**

## Electrical components
Connection between Teensy and MPU9255 is as follows. Teensy connects PC through USB port.
```
 TEENSY4.0 <--> MPU9250
 
 3.3V      <--> VCC
 GND       <--> GND
 SCL       <--> SCL
 SDA       <--> SDA
```
<img src="https://github.com/DonovanZhu/MPU9250_Madgwick_Filter/blob/master/Teensy_MARG_Connection.jpg" width="350">
