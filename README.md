# Digital Race

![alt text](doc/digitalrace.jpg "MagicCar")

Software for the Driverless Car 2017.

[Digital Race](https://cuocduaso.fpt.com.vn/en) 

[FPT Digital Race Youtube Channel](https://www.youtube.com/watch?v=ReT8AF0dVFs)

## Setup Instructions

### Contents
1. [Install Prerequisites](#1-install-prerequisites)
2. [Clone repository](#2-clone-or-fork-repositories)
3. [Install Dependencies](#3


### 1. Install Prerequisites
1. __Install [Ubuntu 16.04]
2. __Install required packages__

##install CMake:
$ sudo apt-get install software-properties-common
$ sudo add-apt-repository ppa:george-edison55/cmake-3.x
$ sudo apt-get update
$ sudo apt-get install cmake
**********************************
##Cài opencv theo hướng dẫn sau:
http://www.jackyle.xyz/2017/12/cai-at-opencv-c-va-python-tren-ubuntu.html

**********************************
##install Astra Camera Driver and OpenNI2:
Tải cái này về rồi giải nén: https://www.dropbox.com/sh/ou49febb83m476d/AADqCQuI3agPOdhyuihl0NHMa?dl=0&preview=OpenNI-Linux-x64-2.3.zip
 
run install.sh to generate OpenNIDevEnvironment, which contains OpenNI development environment 

$ sudo chmod a+x install.sh
$ sudo ./install.sh

please replug in the device for usb-register
add environment variables.

$ source OpenNIDevEnvironment


********************************************
##install I2C For JetsonTK1

$ sudo apt-get install -y i2c-tools
$ apt-cache policy i2c-tools

********************************************
##install GIT

$ sudo apt-get install git

********************************************
##install PWM Servo Driver Board 

$ sudo apt-get install libi2c-dev i2c-tools
$ sudo i2cdetect -y -r 1

#JHPWMDriver Install
Set time and date first
  
### 2. Clone or Fork Repositories
### 3. Install AutoRally ROS Dependencies
### 4. Testing & Running

Test Camera
$ cd ‘/home/ubuntu/Ubuntu/carControl_astra/openni_opencv/src’
$ cmake .
$ make
$ ./test-openni-opencv

Test Servo, I2C 
$ cd ‘/home/ubuntu/Ubuntu/JHPWMDriver/example


$ make
$ sudo ./servoExample
**********************************************
## Theo dõi các ví dụ ở link sau:
https://github.com/taohatemi/Begin.git



