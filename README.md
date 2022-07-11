# oak-camera-setup

Steps to Connect To Camera:
Connect OAK Camera to Injector, plug injector into switch. Use adapter to connect Tablet/Phone to switch.
Go To Settings on the Tablet/Phone and enable Ethernet Tethering/
Download Termux
If Termux says “repository under maintenance” use this tutorial.
If you get any other error try entering, “pkg upgrade”
Obtain the Camera IP Address by typing in these commands into Termux. 
Go here for the full tutorial.
Enter: Pkg install nmap
Enter: Ifconfig
Look for eth0 and inet addr: for Your IP address
Enter: nmap -sn (Your IP address, but replace last digit with 0) /24
Example: nmap -sn 192.168.207.0/24
All ethernet devices and their IP addresses should be shown.

SSH into the camera
Enter: pkg install openssh
Enter: ssh pi@(OAK IP Address) -X. 
Go here for more details.
