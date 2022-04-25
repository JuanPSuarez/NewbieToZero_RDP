# NewbieToZero_RDP
A step-by-step new friendly guide for Remote Desktop Windows machines anywhere.

************************************ WIP ************************************

Hi, in this (quite) simple guide, I'll show you my step by step on how to create a VPN, connecting trought the internet, sending a Wake-On-Lan package to turn on your computer and using remote desktop from almost anywhere.

We'll work with different concepts such us like:

	• VPN
	• LAN
	• WAN
	• RDP
	• Windows and Linux Terminal


Thanks to the easy setup of ZeroTierOne, we can create this Virtual Private Netowrk over the Internet. You can also use Tailscale, you can read this guide (soon™).

Let's get started!


What you would need:

	• Raspberry Pi 4gb (or any mini pc that can run linux) 
	• Desktop or Laptop 
	• Ethernet cable 
	• ZeroTierOne (free)!

Here we should start installing the software neded in the linux machine:

1. Install raspberry pi os lite (or any other distro that you like)
2. Login set a user and pass (default credentials for rpi: pi / raspberry)

Update and upgrade:
	
	$ sudo apt update
	
	$ sudo apt upgrade
	
3. Install ZeroTierOne:

APT-install:

 	$ curl -s https://install.zerotier.com | sudo bash


(Optional) Installing the snapstore:

	$ sudo apt install snapd
	
Install zero tier with snap:

	$ sudo snap install zerotier
	  
Join the network: 

	$ zerotier-cli join #########
	
Check status: 

	$ zerotier-cli status

4. Install etherwake:

APT-install:

	$ sudo apt install etherwake
	
5. Check interfaces:

Check the ip for wlan0 and eth0:

	$ ifconfig

Now with everything installed, we now shall proceed with the configuration, you'll need:
	• Mac-address of the machine to be conected.
	• Rasperry Pi ip's: wireless (wlan0) and ethernet (eth0)
	• Create a zero tier accound and network.


