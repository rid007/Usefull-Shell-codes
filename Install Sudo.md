## Install sudo in Debian 8 Jessie

###Debian seems to not have sudo installed by default.
Here is how to install sudo and add your username to the sudoers file.

Open the Terminal Click "Activities" Click in the "Type to search..." box Type in "Terminal" and press the [enter] key

Switch to root user Type in the Terminal the following command 
        su root@debian:/home/yourusernamehere#

##Install "sudo"

Now that you are root user within the Terminal lets install "sudo"
Type in the following command...

        apt-get update
        apt-get install sudo

Add your username to the sudo group

    adduser yourusernamehere sudo

Now add your name to /etc/sudoers file

    nano /etc/sudoers

- Scroll down and look for the line "%sudo  ALL=(ALL:ALL) ALL"

- Below that line type in the following...
    
    yourusername  ALL=(ALL:ALL) ALL


-"Ctrl+o" save, "Ctrl+x" exit, then press "y" and then press [enter] to exit and save the file

Now we exit out of the Terminal completely - Type in the following command... exit - then press [enter] - Type exit again... exit - then press [enter] - That should have closed the Terminal application

Now let's open a new Terminal and test to see if sudo is working for your user name - Click "Activities" - Click in the "Type to search..." box - Type in "Terminal" and press the [enter] key - Test sudo by typing the following command...

    sudo ls



- If the output looks like the following...
    yourusernamehere is not in the sudoers file.  This incident will be reported.
- then you might have to start from the beginning of these instructions and try again.

- If the output looks like this...
    Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos
- Your username now has sudo rights, congratulations!

Enjoy!
