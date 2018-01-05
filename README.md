# Arduino-in-ROS
Install Arduino in ROS environment

Refer to https://www.arduino.cc/en/Guide/Linux and http://wiki.ros.org/rosserial_arduino/Tutorials/Arduino%20IDE%20Setup. 

## Install Arduino IDE
Refer to https://www.arduino.cc/en/Guide/Linux. 

Download, extract and install
```
$ sudo ./install.sh
```
Plug in the arduino board and usb cable, check connection 
```
$ ls -l /dev/ttyACM*

you will get something like:

crw-rw---- 1 root dialout 188, 0 5 apr 23.01 ttyACM0

$ sudo usermod -a -G dialout <username> 
```
Replace the <username> to your username. 
  

