# MacOS-DMG-Creator
Create a DMG that looks nice on MacOS only *Compatible with MacOS Catalina!*

Installation
------------

By being a shell script, MacOS-DMG-Creator installation is very simple. Simply download and run.  

> git clone https://github.com/colinjmatt/MacOS-DMG-Creator.git  
> cd MacOS-DMG-Creator  
> ./dmg-create [options]  


Usage
-----

> dmg-create [options...] [output\_name.dmg] [source\_folder]  

All contents of source\_folder will be copied into the disk image.  

**Options:**  

*   **--volname [name]:** set volume name (displayed in the Finder sidebar and window title)  
*   **--volicon [icon.icns]:** set volume icon    
*   **--background [pic.png]:** set folder background image (provide png, gif, jpg)    
*   **--window-pos [x y]:** set position the folder window    
*   **--window-size [width height]:** set size of the folder window    
*   **--text-size [text size]:** set window text size (10-16)    
*   **--icon-size [icon size]:** set window icons size (up to 128)    
*   **--icon [file name] [x y]:** set position of the file's icon    
*   **--hide-extension [file name]:** hide the extension of file    
*   **--custom-icon [file name]/[custom icon]/[sample file] [x y]:** set position and custom icon    
*   **--app-drop-link [x y]:** make a drop link to Applications, at location x, y    
*   **--eula [eula file]:** attach a license file to the dmg    
*   **--no-internet-enable:** disable automatic mount&copy    
*   **--version:** show tool version number    
*   **-h, --help:** display the help  


Example
-------

> \#!/bin/sh  
> test -f Application-Installer.dmg && rm Application-Installer.dmg  
> dmg-create \  
> --volname "Application Installer" \  
> --volicon "application\_icon.icns" \  
> --background "installer\_background.png" \  
> --window-pos 200 120 \  
> --window-size 800 400 \  
> --icon-size 100 \  
> --icon Application.app 200 190 \  
> --hide-extension Application.app \  
> --app-drop-link 600 185 \  
> Application-Installer.dmg \  
> source\_folder/  


Alternatives
------------

* [node-appdmg](https://github.com/LinusU/node-appdmg)
* [dmgbuild](https://pypi.python.org/pypi/dmgbuild)
* see the [StackOverflow question](http://stackoverflow.com/questions/96882/how-do-i-create-a-nice-looking-dmg-for-mac-os-x-using-command-line-tools)
