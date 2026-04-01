README :

To run the User Initialization ( 1_usr_init) do the following :
Open a terminal ( AKA Konsole in KDE ) in the Devuan_ISO directory.
Type the following command for root :

su

This will prompt for root password.

Next use the " ./ " command in front of the 1_usr_init file to run the bash script.
It will look like this :
./1_usr_init

The User Init will install sudo, add the user to sudo and root groups,
then it corrects the /etc/apt/sources.list. During initial setup, this file has a cd/dvd 
initial setup line. The script just comments out the first line, so apt update and apt upgrade
will pull from the deb.devuan.org official updates and upgrades.

When complete it will echo out a prompt to reboot for the changes to take effect.

UPON REBOOT

Open a terminal in the Devuan_ISO directory.
Use the " ./ " command in front of the devuan_programs_installer. It will look like this :
./devuan_programs_installer

When the bash script runs, it will prompt the user for their sudo password ( your login 
password).
Upon starting, the installer runs and update, upgrade, and autoremove of old binaries.

It will then install all of my favorite packages that are compatible. Things like audio/video
editing, music players, web or script editors.

It will then install and configure QEMU-KVM for virtual machines.

It will then install and configure ssh.

After installation, it will prompt the user for a reboot again.

*** END OF SETUP AND CONFIGURATION ***

Congrats, you're all set up!
