# rover
Contains the main control program to run on the Mars rover.

## Dependencies:

- WiringPi (http://wiringpi.com/download-and-install/)
- OpenCV (https://opencv.org/)
- pca9685 (https://github.com/Reinbert/pca9685)
This needs to be cloned into the "include" folder.
- rosserial (http://wiki.ros.org/rosserial_arduino/Tutorials/Arduino%20IDE%20Setup)

## Subscriptions:

Topic:       **hbeat**<br />
Msg type:    std_msgs/Empty<br />
Description: Listens for heartbeat from base station in order to determine whether or not we have lost comms.

Topic:       **cmd_data**<br />
Msg type:    rover/DriveCmd (custom)<br />
Description: Receives speed and steering commands from the base station.

Topic:       **encoders**<br />
Msg type:    rover/RPM (custom)<br />
Description: Receives RPM values reported by the Arduino connected to the wheel encoders.

Topic:		 **ball**<br />
Msg Type:	 rover/Ball (custom)<br />
Description: Receives x,y position and radius of a tennis ball on the webcam video stream.
