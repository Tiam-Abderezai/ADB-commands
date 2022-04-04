# ADB Commands
- Record emulator:
``` bash
# Record
adb shell screenrecord /sdcard/video.mp4
# Put it in desktop
adb pull /sdcard/video.mp4 ~/Desktop/
```
- Debug mode
```
# Clear Debug mode
adb shell am clear-debug-app
```
