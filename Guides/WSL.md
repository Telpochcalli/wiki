# Windows Subsystem for Linux Guide

In this guide we will be reviewing how to download, install and setup
**WSL** and **Ubuntu** (version 20.04 LTS).

1. Enable WSL for Windows:

You need to do a series of steps to enables the linux terminal in your Windows computer;

- To do so follow [this video](https://www.youtube.com/watch?v=n-J9438Mv-s) up to timestamp 4:25.
- And if it is not clear enough compliment it with [this guide](https://www.windowscentral.com/install-windows-subsystem-linux-windows-10).

*You might need to restart your computer multiple times to make sure you
have installed everything correctly.

2. Update Ubuntu terminal: 

Once you succesfully follow the steps of the video and guide of **step 1**
you can open the Ubuntu terminal and start setting it up.

- You might need to update it to be able to run commands so type
`sudo apt-get update && apt-get update`.

3. Download and install [VSCode](https://code.visualstudio.com/download):

**If you have VSCode already installed you can skip this step.**

Too make everything easier we are going to use VSCode in cojunction with
the Ubuntu terminal, that's why having VSCode installed in your computer
is very important.
- You can also watch this [VSCode video guide](https://code.visualstudio.com/learn/get-started/basics) if you are having trouble.

4. Access Ubuntu terminal from VSCode:

After you succesfully download VSCode you can continue setting up your 
terminal following [this link](https://gitlab.com/aruw/controls/taproot/-/wikis/Windows-WSL-Setup)
starting on **step N° 7.**

**¡¡Before following "this link" read step 5!!**

5. Notes to make following [this link](https://gitlab.com/aruw/controls/taproot/-/wikis/Windows-WSL-Setup) easier:

- In **step N° 13.** make sure your download ["gcc-arm-none-eabi-9-2020-q2-update-x86_64-linux.tar.bz2"](https://developer.arm.com/-/media/Files/downloads/gnu-rm/10-2020q2/gcc-arm-none-eabi-10-2020-q2-preview-x86_64-linux.tar.bz2?revision=d78e0fa5-cb1e-47d6-84ce-88f3139deee9&hash=9FA7B58CA538BE61178E11BC0C294667F0AC3A66) not the latest version for your computer.

- In **step N° 13.** you can check these [basic commands in linux](https://www.hostinger.com/tutorials/linux-commands) to make the changing of directories easier.

- In **step N° 13.** to reach you desktop use the command `cd /mnt/c/Users/your_user/Desktop`.

- In **step N° 13.** if you are having trouble unzipping the file through the terminal you can always do it in your desktop or downloaded files.

- In **step N° 14.** you can't just copy your path directly mainly because the slashes are the opposite way, so it is recommended to get to it by using `cd` in Ubuntu terminal.
