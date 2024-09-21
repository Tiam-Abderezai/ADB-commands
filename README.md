# ADB Commands
- General:
``` bash
# List devices:
adb devices
# Get ADB Root permission
adb root
# Get ADB Version
adb --version
# Tap on EditText:
adb shell input keyevent KEYCODE_TAB
# Input text into EditText:
adb shell input text <sometext>
# Uninstall an app
adb uninstall --user 0 com.example.app
# Kill an app
adb shell am force-stop com.example.app
# Add/Remove second screen
adb emu multidisplay add 1 2720 720 160 0
adb emu multidisplay del 1
# Turn on/off Nightmode
adb shell "cmd uimode night yes"
adb shell "cmd uimode night no"
# Show Device Display
adb shell dumpsys window displays
```
- Manipulate Android Components
``` bash
# Start an particular Activity:
adb shell am start -n com.example.app/directories.particular.ParticularActivity
# Start a particular BroadcastReceiver
adb shell am broadcast --user 0 -n com.example.app/com.example.app.ParticularBroadcastReceiver -a com.example.app.services.SomeService.SOME_SCREEN
```


- Record emulator:
``` bash
# Record:
adb shell screenrecord /sdcard/video.mp4
# Put it in desktop:
adb pull /sdcard/video.mp4 ~/Desktop/
```
- Debug mode:
``` bash
# Clear Debug mode:
adb shell am clear-debug-app
```
- Accessibility:
``` bash
# Start a11y service:
adb shell settings put secure enabled_accessibility_services com.google.android.marvin.talkback/com.google.android.marvin.talkback.TalkBackService
# Stop a11y service:
adb shell am force-stop com.google.android.marvin.talkback
```
- Dark mode:
``` bash
# Enable:
adb shell "cmd uimode night yes"
# Disable:
adb shell "cmd uimode night no"
```
- Touch on screen position
``` bash
# Touch on specific screen position:
adb shell input touchscreen tap 700 1453
# Get touchscreen x and y position of areas you tap (0035 = x 0036 = y)
# returns a hex value than when converted to decimal, shows touched coordinates
adb shell getevent | grep -E -o '0035.{0,10}|0036.{0,10}'
```
