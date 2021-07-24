# tv_on_off
Shell script for TV power control from an Android box using CEC commands

Short description: Intercept "Power" button, detect a TV state and toggle it.
Why: Allows to you to turn on/off a TV set using a Android remote control

Advantages:
- No need in TV set remote control.
- No need to switch a remote control to "IR" mode and back.
- Script allows to use remote controls without "IR" mode.
- Android box is always on and can control TV set at any time.

Script requires to configure a button and a remote control input device
Script has to be put into init.d folder.
Usualy, it is /etc/init.d
Under UGOOS firmare (and its clones like Slimbox) it is /sdcard/init.d


To recognize a button code, perform next actions:
(It can require a root permissions sometimes)

1. Open a terminal (it can be ADB shell as well)
2. Run: getevent
3. Press a desired button on your remotel control you want to assign to TV power button
4. Press Ctrl-C in order to break getevent command
5. Copy a code from the third line from the bottom

Open a script file in an editor and change "BUTTON" and "INPUT" variable values to yours.

Put a script into init.d folder and reboot a box.


Remarks:
TV set can react with a delay of 8-10 seconds to second press of the button (Sony devices)
