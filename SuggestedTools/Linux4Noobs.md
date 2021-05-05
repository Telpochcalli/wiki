# Ubuntu:

## Apps

There are different ways to download apps.

The main way to do so, is to install **snaps** (the Linux equivalent to apk apps). You can go into the snapstore (in ubuntu called 'ubuntu software') and search.

Another way to install apps is through a .deb file. You can go to a website and get a .deb file, and by downloading it and saving it into downloads, you can oppen it with your package mannager (in ubuntu 'ubuntu software' will do the work), and it will sinstall all the necesry dependencies.

Another way to install software is through an appimage. An appImage is litterally that, an executable that will have everything it need within itself. The filetype is .appimage (wow so impressive name).

The last way, is through apt. This will require the console and admin privileges. To open terminal, use `CTRL` + `ALT` + `T`, and write `sudo apt intall packageName`, replacing packageName with the package you want to install, for example, cmake. `sudo apt intall cmake`. Put your password, and then enter y to confirm. You can also install .deb packages this way, replacing package for the filepath.

## Files

Files are not stored the same way in linux to how it is on Windows. Linux has more of a MacOS kind of filesystem. 

### Root

Everything starts at the root. This is where the OS is installed. You can go there in the terminal by writing `cd /`. Also, all possible files and locations will be here. Represented by /, it litteraly is the start of everything.

### Home

Home is where you will always start when oppening a terminal. it is defined by a ~, and entering `cd` into the terminal will always lead you here. IT IS NOT THE ROOT, it is where your _user_ is, and using something like '~/downloads' will be a valid directory, where ~ will replace the path towards your user. 

Home will normally be located at: `/home/username`

### Directories

To navigate through directories, you mustkeep in mind that you can use 2 different indicators to help you.

- `.` will retrun the current directory, for example, if you are on documents './important' will make you go into the 'important' file
- `..` will make you go up a directory, for example, if you are on documents '../downloads' will make you go back to home, and then enter downloads. 

##### If you wish, you can use as many .. and . as you need

### Devices

Unlike windows, where every device will be on a letter, linux will mount devices to a folder. Devices will be normally mounted to `/media`, however, you can mount them wherever you like. If a device is not storage, it will not be mounted here, and devices will be mounted to a different location, and depending on the device, a different filetype might represent it. 

So yeah, devices ARE files/folders.

### Using Nautilius

The default GUI file mannager on ubuntu is called nautilus. It is pretty simmilar to MacOS, you can have pinned tabs on the left, and on top, you can see the path you are currently in.

Drag and drop works. double click to oppen files with default app, right click for options... great, the main reason why to use it, is to have a quick way to look at things, but also, unlike any other os, you can open the terminal on the current directory you are on... right click on any part and go to oppen in terminal. A new terminal will oppen with the current directory.

Other useful things might be to oppen nautilos from terminal with administrative permisions, type `sudo nautilus`, and there will be no stopping you to what files you can or can't oppen. To see hissen files, just go into options.

