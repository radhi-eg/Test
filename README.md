# Test
This  repository is for testing 
Try to install Ubuntu server 22.04

Steps 
Download ubuntu server 22.04 iso file from website https://ubuntu.com/download/server
Or 
Download ubuntu 20.04 desktop version
https://releases.ubuntu.com/focal/
	File: ubuntu-20.04.5-desktop-amd64.iso
	Server version: ubuntu-20.04.5-live-server-amd64.iso

If iso file is downloaded to windows, rufus is used to create bootable USB
Download Rufus 3.2 from https://rufus.ie/en/
Minimum of  8 GB USB pendrive is taken and kept formatted.
Open Rufus and plugin USB 
Select the USB drive attached 
Choose iso file that is downloaded
Other options are kept as default and click on start to start bootable USB
Once the USB drive becomes bootable the Rufus will show Ready and click on close button.
Booting up ubuntu OS from the bootable USB 
Insert USB and turn on the system/laptop.
Press F8 or F10 or ESC or F12 (boot key) to go to BIOS options 
USB boot drive has to be chosen under boot menu to start launching ubuntu
https://computingforgeeks.com/install-ubuntu-server-jammy-jellyfish/
Choose language and keyboard
Type of installation to be chosen as ubuntu server and not minimized one
Static IP address for one network interface has to be given under network configuration
Proxy address to connect to internet is available as an option
Configure ubuntu archive mirror
Storage is configured by partitioning entire disk as LVM group and no need to use custom storage layout
The user profile set up has to be created which allows to login to ubuntu system by providing username, server name, password
Install openSSH server to enable secure remote access to the ubuntu server
List of tools/packages are to be selected to install during installation process
Once installation is over, click on reboot now 
Remove the USB pendrive
After restart, provide login credentials and start the system


Task 2: Add a cron job in that desktop to reboot server every 30 min

Steps 

Create cron job with command
crontab -e
30 * * * * root shutdown -r
grep CRON /var/log/syslog can be used to check currently cron job is running  or not.
