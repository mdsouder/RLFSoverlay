# RLFSoverlay
How to set up and use RLFS Overlay (README is a Work in Progress)

# First Time Setup
  
3) Nodejs -> https://nodejs.org/en

4) Clone this Repository (*Recommended to receive updates*) or download ZIP

**Setting up BakkesMod and SOS Plugin**

1) Download BakkesMod for Rocket League from the provided link. You should now have a ZIP called ```BakkedModSetup.zip```.
    * https://bakkesmod.com/download.php

2) Extract the executable file ```BakkesModSetup.exe``` from the ZIP and run it. This will install the BakkesMod Injector Application. 

3) Open BakkesMod Application and then launch Rocket League. On the main menu of Rocket League, verify BakkesMod is installed by pressing F2 for the in game BakkesMod Menu. Once you have confirmed BakkesMod is running in Rocket League, you may now exit the game. 

4) Download SOS Plugin for BakkesMod from the provided link. It is recommended to download the latest version of SOS, at the time of writing is version ```1.6```. The exact link may be found at the bottom of the release section and is titled in the format of ```SOS-Plugin-1.6.0.zip```.

5) Extract the files from the ZIP. You should have a file called ```SOS.dll``` and a ```settings``` folder containing ```SOS.set```. 

6) To install the SOS Files, return to the BakkesMod Application. Under the file tab in the top left, click ```Open BakkesMod Folder```. You are now in the BakkesMod directory. Open the folder ```plugins```. Inside this folder, you will copy/cut ```SOS.dll``` from your extracted files. Open the folder ```settings```. Inside this folder, you will copy/cut ```SOS.set``` from your extracted files.

7) You may close the BakkesMod directory. Open Rocket League and go to the main menu. Verify SOS is installed by pressing F2 for the in game BakkesMod menu and clicking the Plugins Tab towards the top right. Once you have confirmed SOS is installed, you may close the BakkesMod Menu.

8) The last step is to activate the SOS Plugin. Open the BakkesMod developer console. This may be accessed from hitting F6, if that does not work try the ~ key. Enter the command ```plugin load sos``` and run. This should now allow SOS to properly run when being accessed.

**Setting up SOS Relay Master**
