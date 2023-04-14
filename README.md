# mi-projector-fan-mod
Potentially prolong your Mi Smart Compact Projector life by adjusting the default fan speed behavior

This mod is tested on Mi Smart Compact Projector model MJJGTYDS02FM.
It might apply to other projector that uses the same Fengmi projector SDK.
DO AT YOUR OWN RISK! I'M NOT RESPONSIBLE FOR ANY DAMAGES!

# The problem:
Sometimes in a hot day, the projector will overheats and display overheating messages. This will dim the screen and make the fan go full speed. Why don't we make it go full speed everytime?

# The solution:
I found that the Fengmi projectors uses a .json file to set the fan curve, on the Fengmi's test tool, the fan curve can be altered with our own .json loaded from a USB stick. Controllable fan speed are in integer between 0 and 10. The default fan speed is 2 which is slow and quiet, they prioritize noise over temperature.

# The Good:
- Faster fan speed = lower temps
- Lower temps = longer component lifetime (especially the LEDs and DLP chips)
- Because the temps are lower, the projector should not go into the "overheat protection" mode.

# The Bad:
- Possibly lower fan life expectancy (the fan is cheaper and more replaceable than the LED/DLP)
- Louder fan noise
- Higher dust accumulation

# The Steps:
There are some tools that you need to download first:
- Activity Launcher (sideload from .apk)
- You may need to install Sideload Launcher from the PlayStore to launch the Activity Launcher\
- FAT32 formatted flash drive


Step 0:
Prepare your FAT32 formatted USB flash drive, copy the test.json file to the root of the drive. Plug into the USB port on the projector.

Step 1:
Open Activity Launcher, and scroll to the bottom, you'll see an app with Chinese character, tap on it, make sure it expands into com.fengmi.autofocustest.MainActivity. Tap on the activity.
![Screenshot_20230414-162451](https://user-images.githubusercontent.com/12219401/232009201-0aa17b0f-c112-44d6-a7eb-4b1a099b6fa4.png)

Step 2:
Fengmi tools will open with a bunch of Chinese buttons, navigate to the very bottom and tap on the button.
![Screenshot_20230414-161050](https://user-images.githubusercontent.com/12219401/232009522-8b7c5fac-6d3b-4bca-a5e6-063100387e9f.png)

Step 3:
Tap on the 4th button with a letter U on it
![Screenshot_20230414-161105](https://user-images.githubusercontent.com/12219401/232010022-ba581807-3db5-4364-9199-306ac52d7386.png)

You'll see a message like this, and hear that the fan noise is getting louder.
![Screenshot_20230414-161108](https://user-images.githubusercontent.com/12219401/232010177-ffdd5009-0748-4259-b9f5-8c1258fe2266.png)

That means the configuration files has been loaded successfully from the flash drive.

Step 4:
Confirm the newly applied fan speed by tapping the first button on the list:
![Screenshot_20230414-161054](https://user-images.githubusercontent.com/12219401/232010472-ed1c6361-f0eb-49f8-8ef7-93018a64d0e7.png)

The Fan speed should be 8 by default (you can change this on the test.json)
![Screenshot_20230414-161117](https://user-images.githubusercontent.com/12219401/232010487-abbb80ba-c4d3-4ad6-928c-119d546b1f8a.png)

You're done!

Info: To revert to the factory settings, follow step 1 - step 3, tap the 4th button until it shows letter U on the label.

