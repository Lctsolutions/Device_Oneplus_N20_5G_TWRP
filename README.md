# This is a secondary attempt at TWRP tree for OnePlus Nord N20 5G based on the TWRP for OnePlus Nord CE2 Lite 
by Spector0
aka holi

This TWRP works on my devices that are still on a11 , May and July security patched.
Still does not boot to system with TWRP in ramdisk but i used a workaround by putting the TWRP on my active slot and putting my working boot image on my inactive slot and installing bootctl in magisk then using switchslot app to switch slots from android to get to twrp, then do what i need to do in TWRP and then change slots and reboot to get back to system. someone much smarter than me will have to pick this up and finish it. Hopefully someone will. The reason for putting TWRP on the active slot that my system is on, is so that zips will flash correctly, if not, when you flash a zip it wont work because recovery will try to flash it to the wrong slot. its a bit of a pain but it works for me. Feel free to contribute or fork and carry on the project. Thanks Spector0 for helping me and your attempts at the unified kernel and to all others who were part of that and who donated their time to helping me with everything!
Below is just a copy of Spector0's instructions. just keep in mind the above stated workaround. All features are working otherwise.
I literally just swapped out the oscar boot kernel with the stock one from the N20 5G boot image hoping that a simple kernel swap would get it booting to system with TWRP in ramdisk but it seems the issue is a little more complicated than that. i also swapped out dtb and dtbo but no luck still.

Installation:
Note: Backup stock boot image and keep it in your platform tools folder

* Download and extract the Zip file and rename the boot.img to twrp.img(not mandatory)
* reboot the device to bootloader
* Use "fastboot flash boot twrp.img" to flash twrp
* Now reboot to recovery and decrypt
* Copy the stock boot image to internal storage and flash stock boot to both slots
* Now do to "Advanced" option in twrp and select "Flash Current TWRP"

[Optional] press back and install Magisk zip/apk if root is required
Reboot to system
