# clevo-insyde-uefi-settings-show-all
Little guide on how to show all the settings in clevo insyde_h20 uefi.

# first things first
The operations in this guide will most likely unlock __ALL__ settings in this bios. Do __NOT__ do this if you don't have a good reason!
If you think something is wrongly set and you are unsure, just go to load the optimal defaults, or your device may even can't power on!

# values
+ NH50/NHxxRA
    + offset is 0x133
    + value is 0x01
      + tested on hasee_z7m-ct5na(~~oem modded bios~~)

# generic steps
1.  Download the modded "uefi shell" here https://github.com/datasone/grub-mod-setup_var ,and save it in a bootable device
2.  restart into uefi main menu(from windows advanced reboot or press f2 after power on),choose "Boot from file",then choose it.
3.  run "setup_var [offset]" "setup_var2 [offset]" "setup_var_3 [offset]",and find out which command can find a GUID that has a name of "Setup".(Just ignore the mismatch message and look for "Setup")
4. run that command multiple times,and write down all the current values of the offset of all GUID.
5. run "that_command [offset] [value]".If the command set the value on the right GUID,go ahead.If not,use the same command with values you previously saved to set them back.Try until you set in the right GUID and other GUID are still default.
6. Run "quit""exit" or other to exit to the uefi main menu.
7. Start the setup utility,and see if the magic happens.

# well
Please improve this if you find such values on other models。And sorry for my bad english,any contribution is welcome！
