# LinuxTips

## How to Get rid of the login keyring password

Open terminal and type:

```seahorse```

You have to go to ```Passwords``` Tab, and there you will se a folder: ```Passwords: login```  

Right Click and then ```Change Password```. Enter your old password, and leave blank the new password fields.

Now you can try rebooting, it shouldn't appear now!

https://community.linuxmint.com/tutorial/view/916

## Install Redshift

`
sudo apt-get install redshift redshift-gtk
`

**if you get errors like...**

Failed to run Redshift
Trying location provider ```geoclue2…

Unable to connect to GeoClue.

Unable to get location from provider.```


...install this:

`
sudo apt-get install geoclue-2.0
`
## Convert audiobooks to .mp3

`
ffmpeg -i downloaded_file.aa output.mp3
`
## GNU/Linux booting to CLI, no GUI

You can type `startx` to start the system with the available GUI options.

`
sudo dpkg-reconfigure lightdm
`

<br>
<img src="https://i.imgur.com/qAcWGIR.jpg" style="zoom:50%;" alt="reconfigure-lightdm" />

## Reminna - Protocol plugin RDP is not installed

```console
sudo apt get update -y
sudo apt get upgrade -y
sudo add-apt-repository ppa:remmina-ppa-team/remmina-master
sudo apt get update -y
sudo apt get install remmina remmina-plugin-rdp
sudo apt get purge remmina-* -y
sudo apt get autoremove -y
sudo apt get install remmina remmina-plugin-vnc remmina-plugin-rdp -y
sudo killall remmina
sudo apt get purge remmina* -y
rm -Rf /home/`whoami`/.remmina/remmina.pref -y
sudo add-apt-repository ppa:remmina-ppa-team/remmina-next -y
sudo apt get update -y
sudo apt get install remmina* -y
sudo apt get install remmina remmina-plugin-vnc remmina-plugin-rdp -y
sudo apt get install remmina-plugin-rdp
```


## Difference between init and shutdown

| Init  	|Description   	|Shutdown   	|Description|  
|---	    |---	          |---	    	  |---        |
|init 0   |Shuts down the system whithout calling any procces. Can be perfomed only by the SU.|shutdown|SAFELY shuts down the system. Can be performed by any user.|
|||shutdown now|
|||shutdown -p now|Powers off the machine.|
|||shutdown -H|Halts the system.|
|||shutdown 13:20|Schedules shutdown for 13:20.|
|init 1|Single user mode or emergency mode means no network no multitasking is present in this mode only root has access in this runlevel.|||
|init 2|No network but multitasking support is present.|||
|init 3|Network is present multitasking is present but with out GUI .|||
|init 4|It is similar to runlevel 3; It is reserved for other purposes in research.Network is present multitasking and GUI is present with sound etc.|||
|init 5|This runlevel is defined to system restart.|||
|init 6   |Restarts the system whithout calling any procces. Can be perfomed only by the SU.|shutdown -r|SAFELY restarts the system. Can be performed by any user.|
|||shutdown -r09:35|Reboot the machine at 09:35am.|
|||shutdown -c|Cancel a pending shutdown.|
|init s|Tells the init command to enter the maintenance mode. When the system enters maintenance mode from another run level, only the system console is used as the terminal.|||
|init S|Same as init s.|||
|init m|Same as init s and init S.|||
|init M|Same as init s or init S or init m.|||

## Halt command
**Halt** instructs the hardware to stop all CPU functions, but leaves it powered on. You can use it to get the system to a state where you can perform low level maintenance.


| Halt          | Description                           |
| ------------- | ------------------------------------- |
|               |                                       |
| halt          | Halts the machine (complete shutdown) |
| halt -p       | Powers off the machine                |
| halt --reboot | Reboot the machine                    |


## Power off Command
**Poweroff** sends an ACPI signal which instructs the system to power down.

| Poweroff          | Description            |
| ----------------- | ---------------------- |
|                   |                        |
| poweroff          | Powers off the machine |
| poweroff --halt   | Halts the machine      |
| poweroff --reboot | Reboot the machine     |


## Reboot Command
**Reboot** instructs the system to restart.

| Reboot        | Description            |
| ------------- | ---------------------- |
| reboot        | Reboots the machine    |
| reboot --halt | Halts the machine      |
| reboot -p     | Powers off the machine |

