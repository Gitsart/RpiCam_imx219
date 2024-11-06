# RpiCam_imx219
Hands on with the new Raspberri Pi5 and arducam 8MP imx219. ReamME for installation details.
imx219 equipped arducam 8MP camera is used here. The native camera guide for Raspberry pi will help you go through the hardware and connection details.
https://www.raspberrypi.com/documentation/computers/camera_software.html
you have to navigate in the raspberry pi terminal after setting up to :
$ sudo nano /boot/firmware/config.txt
edit the file:
camera_auto_detect = 0 // normally 1

under [all] add the line:

dtoverlay=imx219
save exit and reboot the pi.

If the connections are right with :
$ libcamera-vid timeout=0 , or rpicam-vid

we can see a video feed of the camera.

For more syntax type in libcamera--help in your shell.
