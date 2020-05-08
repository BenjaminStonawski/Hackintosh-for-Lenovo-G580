# Hackintosh Guide for Lenovo G580

This is a guide for Lenovo G580 if you want to install Hackintosh into it.

# Creating the USB Disk

1.	Download one of the macOS versions from there: https://github.com/BenjaminStonawski/Hackintosh-for-Lenovo-G580/tree/master/macOS%20Download%20links

2.	Use TransMac to for creating the USB Installer. This video could help you: https://www.youtube.com/watch?v=T_moO9c30c4

3.	Download “MiniTool Partition Wizard” and “Explorer++” for copying Clover to the USB Drive. In MiniTool, search the EFI partition of your pendrive then hide and unhide it. After that, run Explorer++ as administrator, find the EFI partition, if there is no “EFI” folder, create one. After that download Clover zip from there: https://github.com/CloverHackyColor/CloverBootloader/releases. After that, copy these files into the “EFI” folder, then delete everything that is in the “CLOVER” folder and then, move these file to there: https://github.com/BenjaminStonawski/Hackintosh-for-Lenovo-G580/tree/master/Clover%20config. This video could help you with mounting the EFI partition: https://www.youtube.com/watch?v=zx6HKkWequI






# Booting and installing

4.	Now, boot the USB Disk. You need to press the Novo button -> Boot Menu -> select “EFI USB - xy”.

5.	Now select: “Boot macOS Installer from Install macOS xy” (xy = the version of your macOS). In the installer format your Hard Drive, name it to: “Macintosh HD” (EVERYTHING WILL BE DELETED FROM IT!!!) and then, you can now install Hackintosh. After 30 minutes your computer should restart, and now don’t boot the “Boot macOS Installer from Install macOS XY” you should boot to “Boot macOS Installer from Macintosh HD” now. If the installer restarts, you should boot to Macintosh HD again.

# Fixing and Installing drivers

6.	After a successful installation, you are in macOS! But we are not done yet. If you don’t have a macOS-compatible WiFi card, use your ethernet, and if you want to use WiFi and don’t want to buy a WiFi card, buy a USB WiFi, and install this driver: https://github.com/BenjaminStonawski/Hackintosh-for-Lenovo-G580/tree/master/WiFi%20USB


7.	Download GenSMBIOS: https://github.com/corpnewt/GenSMBIOS. After you downloaded it, open Terminal, and write these commands:
1.	cd /xy/GenSMBIOS/
2.	chmod +x GenSMBIOS.command
3.	./GenSMBIOS.command
          (xy = the path where you downloaded GenSMBIOS. It’s    maybe ~/Downloads/.

8.	After that, if you are on Sierra or High Sierra, then congrats, you are done! But if you have Mojave, download this driver: https://github.com/BenjaminStonawski/Hackintosh-for-Lenovo-G580/tree/master/HD%20Graphics%203000%20-%20Mojave
          And if you are on Catalina, download this driver:       https://github.com/BenjaminStonawski/Hackintosh-for-Lenovo-G580/tree/master/HD%20Graphics%203000%20-%20Catalina
Then restart.

9.	Now download DPCIManager from there: https://sourceforge.net/projects/dpcimanager/
Run the app. If you see this: 
![Modular Image Creation]( https://media.discordapp.net/attachments/697226271222005803/708379985718542456/unknown.png)
(en0, Built-in is ticked), then you are done. But if it’s not en0 or its not built-in, you should run this command from terminal: 
sudo rm /Library/Preferences/SystemConfiguration/NetworkInterfaces.plist.

# Well done!

10.	After a restart you have a fully working IdeaHack G580! Congratulations!

# Something went wrong?

If you have any questions, you can find me on Twitter my name is: @YtBenjike

Benjamin Stonawski 


