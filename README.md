*****************************************************************************************************************
	STAR CITIZEN TARGET Profile
		Supports the below combinations of Thrustmaster products:
		- Thrustmaster Warthog HOTAS (Fully Supported)
		- Thrustmaster FCS HOTAS (WIP)
		- Thrustmaster TM16000 Dual sticks (Supported)
		- Thrustmaster Warthog Dual sticks (WIP)
		- Thrustmaster Rudder Pedals (Supported)
		- Thrustmaster MFDs (WIP)
		- Right Stick (Warthog or TM16000) with Keyboard (WIP)
		- Left Stick (Warthog or TM16000) with Mouse (WIP)
		
	Written by qp
 		https://robertsspaceindustries.com/citizens/q-p

*****************************************************************************************************************
Version Info
Updated for Star Citizen 3.0 PTU
Last Update: Nov 27 2017
*****************************************************************************************************************
This profile is a work-in-progress
*****************************************************************************************************************
Currently given testing access to members of Old Blood and Guts gaming community
Learn more at oldbloodandguts.com
you can also contact me on Discord qp#8888
*****************************************************************************************************************
Installation
*****************************************************************************************************************
Download a .zip from github that contains all needed files. Extract to a folder of your choosing.

1. Copy qp.xml from the extracted folder into your StarCitizen\USER\Controls\Mappings folder. If the folder does not exist, make sure you run StarCitizen once and then exit the game.
2. Open TARGET SCRIPT EDITOR. Go to MENU and select OPEN.
3. Navigate to the extracted folder that contains qp.tmc file and open this file.
4. Press the TOOLS menu and select the COMPILE button.
5. You will see a list of files being opened as it reads qp.xml. Click on the qp_settings.tmh file and edit as required. Save changes and press COMPILE again.
6. You should see "Compile Succeeded." as a message on the bottom half of TARGET SCRIPT EDITOR.
7. Press RUN. You should see "main returned 0" - this means everything is OK.
8. Start Star Citizen 3.0 PTU. Once in the main menu screen, press "~" to open the in-game console.
9. Type the command "pp_rebindkeys " include a space at the end. you can press "tab" to auto-complete. This will reset all keybindings to defaults.
10. Type the command "pp_rebindkeys qp". You should see "njoy" message. You may close the console by pressing "~". 
11. Profit! njoy :)

Recommended extra step: In TARGET Script Editor under the TOOLS menu, click on OPTIONS and then click the Tab EDITOR. Select the first option so the script auto-loads every time you open the script editor, you will only have to click RUN.

You may find the latest version of qp's Thrustmaster Joystick Button Mappings here: https://1drv.ms/x/s!AuKEmoCXDlmvwdRZCDnmGPjJ3Nmfgw

*****************************************************************************************************************
Known Issues:
*****************************************************************************************************************
- You need to keep ESP turned off when flying, this way it will only engage when firing at a target.
- Various controls like analog view zoom are broken in current PTU builds.
- Star Citizen might not load correctly the deadzones from qp.xml. Make sure your in-game deadzones are all at 0 value and all curves for all axis are set to 1.0. This is not the default for the game, you need to ensure it is applied until CIG fixes their controller support.
