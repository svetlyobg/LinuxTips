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

## Difference between init and shutdown

| Init  	|Dicription   	|Shutdown   	|Dicription|  
|---	    |---	    |---	    	|---    |
|init 0   |  Matches the Pattern 	   	|^OFF$  |
|init 6   | 
