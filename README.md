# RLFSoverlay
How to set up and use RLFS Overlay

**Current Version: 2.3 - June 14, 2023**
* View wiki for versions and changelogs -> https://github.com/mdsouder/RLFSoverlay/wiki

# First Time Setup

### Setting up BakkesMod and SOS Plugin

1) Download BakkesMod for Rocket League from the provided link. You should now have a ZIP called ```BakkedModSetup.zip```.
    * https://bakkesmod.com/download.php

2) Extract the executable file ```BakkesModSetup.exe``` from the ZIP and run it. This will install the BakkesMod Injector Application. 

3) Open BakkesMod Application and then launch Rocket League. On the main menu of Rocket League, verify BakkesMod is installed by pressing F2 for the in game BakkesMod Menu. Once you have confirmed BakkesMod is running in Rocket League, you may now exit the game. 

4) Download SOS Plugin for BakkesMod from the provided link. It is recommended to download the latest version of SOS, at the time of writing is version ```1.6```. The exact link may be found at the bottom of the release section and is titled in the format of ```SOS-Plugin-1.6.0.zip```.

5) Extract the files from the ZIP. You should have a file called ```SOS.dll``` and a ```settings``` folder containing ```SOS.set```. 

6) To install the SOS Files, return to the BakkesMod Application. Under the file tab in the top left, click ```Open BakkesMod Folder```. You are now in the BakkesMod directory. Open the folder ```plugins```. Inside this folder, you will copy/cut ```SOS.dll``` from your extracted files. Open the folder ```settings```. Inside this folder, you will copy/cut ```SOS.set``` from your extracted files.

7) You may close the BakkesMod directory. Open Rocket League and go to the main menu. Verify SOS is installed by pressing F2 for the in game BakkesMod menu and clicking the Plugins Tab towards the top right. Once you have confirmed SOS is installed, you may close the BakkesMod Menu.

8) The last step is to activate the SOS Plugin. Open the BakkesMod developer console. This may be accessed from hitting F6, if that does not work try the ~ key. Enter the command ```plugin load sos``` and run. This should now allow SOS to properly run when being accessed.

### Setting up SOS Relay Master

1) First download the ZIP of this project, or as recommended to clone this repository. Save this project in an easy to reach directory for future use.

2) Download Node.js from the provided link. It is recommended to download the latest version. Once downloaded, run the installer and follow the steps to install Node.js.
    * https://nodejs.org/en
3) Open Command Prompt. Navigate in Command Prompt to this project's directory, wherever you may have saved it. Once inside `RLFSoverlay`, navigate into the folder `sos-ws-relay-master`.

4) Inside `sos-ws-relay-master`, enter the command `npm install` and run. If there are any suggestions from npm to update, you may ignore.

5) Still inside `sos-ws-relay-master`, enter the command `node ws-relay.js` and run. You will be given three prompts, just hit the enter key at each prompt as everything is setup to use the given defaults. Once past the prompts, a Websocket will be opened and an error message may be presented. If Rocket League is not running or you did not run the `plugin load sos` command, this error is normal. You may leave this command prompt open and running. To end the Relay at any time, use the keys ```Ctrl+C```.

6) To successfully connect and start receving game state messages, first open Rocket League again. Once Rocket League has launched, you should see a success message that Rocket League has connected on the given port. To see messages being output, start a private match with bots. 3v3 is recommended as the Rosters portion of the layout handles that many players. Once you hit the team select screen, the command window should start to log messages that are being received from the game. To see more types of messages, start spectating and you can observe the different types of messages.

### Setting up RLFS Overlay in OBS

**As a note, some steps will be marked as necessary to use the overlay, and other steps will be recommendations to organize the scene.**

1) Download OBS from the provided link. It is recommended to download the latest version. Once downloaded, run the installer and follow the steps to install OBS.
    * https://obsproject.com/download

2) Launch OBS. If it is the first time with OBS, you will need to create a new scene, otherwise it is recommended to do so.

3) Within the new scene, you will need to add a new source. This may either be a Game Capture or Display Capture to get the Rocket League gameplay.

4) To add the Overlay, we will need to create Five Browser sources. It will be necessary that in the properties of these Browser sources, the ```local file``` checkbox must be selected, the width set to 1920, and the height set to 1080. These Browser sources should be above the Rocket League Capture Source in OBS.

5) Still within Browser source properties, we should have ```local file``` box checked. Click ```Browse``` on the right side to start to find our overlay components. In the file explorer, navigate to this projects directory and open the folder ```componentOverlays```. Select one of the files for the Browser source. It is recommended to name the Browser source as the name of the component you selected for it. Repeat this for each Browser source/overlay file.

6) It is recommended to group all the overlay components in a single folder within sources to easily minimize the browsers or hide the overlay on stream.

7) You should still have Rocket League running and the SOS Relay Master running. Start a private match with 3v3 Bots and spectate. The overlay should start to display all game data and events in real time. If nothing is happening, select each individual broswer source and click ```Refresh``` below the stream preview, or ```Refresh cache of the current page``` in the source properties. 

8) You have now set up the RLFS Overlay!

# How To Start Up Overlay

1) Launch BakkesMod Application.

2) Open Command Prompt. Navigate to the ```sos-ws-relay-master``` folder inside this project's directory. Enter the command ```node ws-relay.js``` and run. Skip each prompt until it is trying to connect.

3) Launch Rocket League. Join Private Match and Spectate.

4) Open OBS and navigate to RLFS Scene. Refresh components as necessary.

# End Credits

Here are a few additional sources for any help in setting up different requirements for this overlay.
   * BakkesMod -> https://www.youtube.com/watch?v=X290anUi9qE
   * SOS Plugin -> https://www.youtube.com/watch?v=QE816DBuwI4

Developed and Maintained by Matthew Souder. Open to any inquires.
