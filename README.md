# ADB Commands
- General:
``` bash
# List devices:
adb devices
# Tap on EditText:
adb shell input keyevent KEYCODE_TAB
# Input text into EditText:
adb shell input text <sometext>
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
```
