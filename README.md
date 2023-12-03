# Rotate-Screen
# Rotate The Screen On  A Linux Machine
# "Digital Picture Frames" would not display in Landscape view with a Raspberry PI build called "DynaFrame"
# Use case was for a Raspberry PI

To rotate the screen 90 degrees right:
--------------------------------------

Raspbian, you can use one of the following methods:
---------------------------------------------------
If you use the desktop environment, you can use the Screen Configuration tool. To access this tool, click 
the Pi icon in the top-left corner of the screen, then hover over Preferences and click Screen Configuration. 
Right-click the display you want to rotate, hover over Orientation, and click Right. Click the green tick button to confirm the change1

For most other Linux machines:
------------------------------
If you are using the terminal or SSH, you can use the xrandr command. To do this, run the following command:
DISPLAY=:0 xrandr --output HDMI-1 --rotate right

This command will rotate the screen to the right for the HDMI-1 output. You can check the name of your output by running DISPLAY=:0 xrandr without any arguments2

If you want to rotate the screen permanently, you can edit the /boot/config.txt file. To do this, run the following command:
sudo nano /boot/config.txt

Then, add the following line at the bottom of the file:

display_rotate=3

This option will rotate the screen by 270 degrees, which is equivalent to rotating by 90 degrees right. Save and exit the file, then reboot your Raspberry Pi for the changes to take effect34

I hope this helps. 😊

# Simple Fix #Linux Kernal Modification
