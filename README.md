# Pre1.9_Wall_Macro

This is built on top of Nieuh's most recent Pre 1.9 wall macro and offers better pausing stability, better instance lock + instance play logic, and offers a better overall user experience when resetting.

Things you need to know:

- There is a bug that happens often where a given instance will "think" that you are active on that instance, even if that instance is not active. This causes your mouse cursor to move to the top of the screen and can be annoying and also illegal if it happens while you are playing another instance. There are features in this macro that fix this but sometimes it still happens upon instance launch, which in that case, you will need to tab into every instance that is launched. (I had to figure all of that out the hard way)

- You can use the sleep background mod with this macro, you just have to go into the config settings and disable the "polling_rate_limit" . Also if you are tech savy with sleepbackround, this macro supports the sleepbg.lock feature.

- PauseOnLostFocus must be disabled for every instance

- If you don't know how to setup multi instance, watch spinnakers video: https://www.youtube.com/watch?v=FBqtOb3smOw

Mods required:

- Tab Focus
- Atum
- StateOutput

Optional (highly recommended):

- SleepBackground

# For People Interested In The Tech:

- This macro uses the State Output mod files to recognize the current status of an instance instead of pixel searching, which allows for bulletproof stability even at very low pause delays.

- If you lock multiple instances, play an instance, and reset, it will keep activating the next locked instance upon a reset until there are no more locked instances, it will go back to the wall screen after the last locked instance is reset.

- There is a setting called "obsCorrecter", all this does is loop the OBS key 4 times with the obsDelay variable at the end of each loop to ensure the scenes get active. Its rare you would need this but if your computer lags extremely bad, then you might need to enable this. Do not enable this as a default, try to avoid this setting as best as possible. It will increase the delay between you clicking play on an instance, and it actually playing the instance.

- This macro will create a null file called "sleepbg.lock" in your user directory when you are playing an instance, and delete it when you are not. This is used for the sleepbackground feature for wall resetting vs in game play
