# OAK-D CM4 POE Camera Setup

### Connect Tablet to Camera 
![camera setup](https://docs.google.com/drawings/d/e/2PACX-1vRyIKDyIW1dKc1ZNlByO9vhbYpe7WN5FKFMsWFR1a4VKudgFgmFSWMJjS2dsklb3mQRJP6mQPw0Um4X/pub?w=480&h=360)
### Go To Settings on the Tablet and enable Ethernet Tethering
1. Open Settings
2. In the top right, click the search icon and search for Ethernet Tethering
3. Enable Ethernet Tethering (Adapter Must Be Connected To Tablet)
### Download Termux
- If Termux says `repository under maintenance` use this tutorial -> https://www.learntermux.tech/2021/08/termux-repository-under-maintenance.html
- If you get any other error try entering into terminal, `pkg upgrade`
### Obtain the Camera's IP Address by typing in these commands into Termux. 
- For Full tutorial go here -> https://itsfoss.com/how-to-find-what-devices-are-connected-to-network-in-ubuntu
1. `Pkg install nmap`
2. `Ifconfig`
3. Look for `eth0` and `inet addr`: for Your IP address
4. `nmap -sn `(Your IP address, but replace last digit with 0)`/24`
   Example: `nmap -sn 123.123.123.0/24`
5. All ethernet devices and the Camera's IP addresses should be shown.

### SSH into the camera
1. Enter: `pkg install openssh`
2. Enter: `ssh pi@(OAK IP Address) -X`
3. If that does not work click this link for more details -> https://docs.luxonis.com/projects/hardware/en/latest/pages/guides/raspberrypi.html#ssh-into-the-rpi
