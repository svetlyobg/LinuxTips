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
Trying location provider `geoclue2’…

Unable to connect to GeoClue.

Unable to get location from provider.`


...install this:
`
sudo apt-get install geoclue-2.0
`
