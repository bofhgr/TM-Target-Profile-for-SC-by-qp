*****************************************************************************************************************
	STAR CITIZEN TARGET Profile by qp
		Supports the below combinations of Thrustmaster products:
		- Thrustmaster Warthog HOTAS (Fully Supported)
		- Thrustmaster Rudder Pedals (Fully Supported)
		- Thrustmaster TM16000 Dual sticks (Fully Supported)
		- Thrustmaster FCS HOTAS (WIP)
		- Thrustmaster MFDs (TBA)
		- Right Stick (Warthog or TM16000) with Keyboard (TBA)
		- Left Stick (Warthog or TM16000) with Mouse (TBA)
		- Thrustmaster Warthog Dual sticks (TBA)
		
	Written by qp
 		https://robertsspaceindustries.com/citizens/q-p
	

*****************************************************************************************************************
Version Info
Updated for Star Citizen 3.0 PTU build 695052
Last Update: Dec 23rd 2017


*****************************************************************************************************************
This profile is a work-in-progress currently under BETA Testing within my org. Please do not share without permission :)

	Feature list:
	- Supports all TM products, combining them into 1 virtual joystick that makes life easier.
	- Customize-able Flight mode settings (currently 4 distinct flight modes)
	- Designed for true Hands-on experience, you won't be needing your keyboard/mouse with HOTAS and HOSAS full support.
	- Functions and macros customized for the most demanding users with no compromise.
	- Can be expanded to include specific user requested settings, mappings and functions/macros.
	- Cleanly written code with lots of annotations so you can learn how to code by editing this and reading the comments
	


*****************************************************************************************************************
This script is provided as-is with the intent to help the Star Citizen community enjoy the most of their TM controllers with the game.
This script is under constant development since Alpha 1.3 version (~2015) and has seen limited beta-testing by my orgmates. It was initially released for public with SC 3.0 Live.
I am continuing to make improvements and customizations and the script will continue to evolve and be available for free via my github page.
To support future development of this script, please visit my patreon page https://www.patreon.com/qp
I will be giving select patreon members the ability to request code changes or customizations in the near future, please contact me if you would like to know more.
Please feel free to reach me at Discord @qp#8888 for any comments and feedback.
*****************************************************************************************************************



*****************************************************************************************************************
Installation
*****************************************************************************************************************
Download a .zip from github that contains all needed files. The latest version can always be downloaded from: https://github.com/bofhgr/TM-Target-Profile-for-SC-by-qp/archive/master.zip

Extract to a folder of your choosing.

1. Copy qp.xml from the extracted folder into your StarCitizen\USER\Controls\Mappings folder. If the folder does not exist, make sure you run StarCitizen once and then exit the game.
2. Open TARGET SCRIPT EDITOR. Go to MENU and select OPEN.
3. Navigate to the extracted folder that contains qp.tmc file and open this file.
4. Press the TOOLS menu and select the COMPILE button. You will see a list of files being opened as TARGET SCRIPT EDITOR loads up qp.tmc.
5. Click on the qp_settings.tmh file from the list, and edit as required. Click the Save icon and click on qp.tmc and then press COMPILE again, the * next to qp_settings.tmh will go away, meaning your changes are saved.
6. You should see "Compile Succeeded." as a message on the bottom half of TARGET SCRIPT EDITOR.
7. Press RUN. You should see "main returned 0" - this means everything is OK. To test out-of-game you may press Windows Key and type "game" - select the "setup USB Game controllers". You should only see "Thrustmaster Combined" as your only joystick, no other TM products should be listed there. If not, stop and re-run the script (sometimes joysticks won't properly initialize, you might need to reboot if stop/run a couple times does not fix it)
8. Launch Star Citizen 3.0. Once in the main menu screen, press "~" to open the in-game console.
9. Type the command "pp_rebindkeys " include a space at the end and press enter. You can press "tab" to auto-complete. This will reset all keybindings to defaults.
10. Type the command "pp_rebindkeys qp". You should see "njoy" message. You may close the console by pressing "~". 
11. Profit! njoy :)

Recommended extra step: In TARGET Script Editor under the TOOLS menu, click on OPTIONS and then click the Tab EDITOR. Select the first option so the script auto-loads every time you open the script editor, you will only have to click RUN.

Recommended extra step: Do the below if you face issues with your joysticks not responding after a few minutes of running the script. This is a known issue with Windows Power Management for USB devices that assumes the joysticks are safe to power off when they detect the combined virtual joystick that this script creates. To disable this behaviour you have to do the following once. You will have to re-do these steps if you switch your joystick to another USB slot.

1. Press Windows Key + R to open the run menu. Type Regedit and press enter to open up the Windows Registry Editor.
2. Navigate from the left side folder-like structure to the location: Computer \ HKEY_LOCAL_MACHINE \ SYSTEM \ CurrentControlSet \ Enum \ USB
3. Navigate a few items down the USB tree until you see the ones starting with "VID_044..." These are the ThrustMaster Products.
4. For device represented on this tree starting with VID_044... expand the tree and go to Device Parameters
5. On the right side of regedit window you will see two settings you need to change from 1 to 0 AllowIdlelrplnD3 and EnhancedPowerManagementEnabled
6. To change these settings just double-click the parameter and on the Edit DWORD window type in Value Data: 0 instead of 1.
7. Click OK to close the DWORD edit and repeat for both parameters and for each joystick device.
8. Reboot your PC to apply the change and run the script normally from now on.

You may find the latest version of qp's Thrustmaster Joystick Button Mappings here: https://1drv.ms/x/s!AuKEmoCXDlmvwdRZCDnmGPjJ3Nmfgw

*****************************************************************************************************************
Known Issues:
*****************************************************************************************************************
- Targeting Turrets still is not great, CIG uses the look axis to control them instead of aim axis, some bugs there for sure.
- Various controls like analog view zoom are broken in current PTU builds.
- (Fixed) Star Citizen might not load correctly the deadzones from qp.xml. Make sure your in-game deadzones are all at 0 value and all curves for all axis are set to 1.0. This is not the default for the game, you need to ensure it is applied until CIG fixes their controller support.
- Mobiglass interaction and mouse movement is not fully supported yet, but you can still use the new Augmented Reality system with your setup.
- Detailed layout and operation manual for how to best use these control schemes is being developed and will arrive in video format at a later date. Currently available in crude spreadsheet form (links above).
