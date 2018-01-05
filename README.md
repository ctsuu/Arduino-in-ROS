# Arduino-in-ROS
Install Arduino in ROS environment



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
Logout and login again, you should be able to access your arduino board. 
  
## Install rosserial_arduino 
Refer to http://wiki.ros.org/rosserial_arduino/Tutorials/Arduino%20IDE%20Setup. 
```
$ sudo apt-get update
$ sudo apt-get upgrade
$ sudo apt-get install ros-kinetic-rosserial-arduino
$ sudo apt-get install ros-kinetic-rosserial
$ sudo apt-get install arduino-mk
```
Make sketchbook for arduino projects.
```
$ mkdir sketchbook
$ cd sketchbook/
$ ls
make sure ros_lib is not there, or you can remove it
$ rm -rf ros_lib
$ rosrun rosserial_arduino make_libraries.py .
```
The program will create new ros_lib under sketchbook. 

## Install rosserial_lib in arduino IDE

Reboot the computer, open the arduino IDE, you would not see the new ros_lib in the example manual. 
You need goto sketch>include library>Manager Libraries>Library Manager, search for "rosserial" and install. 

