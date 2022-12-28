# Chromium MacOS build with proprietary codecs (ARM64)

Download 
[Chromium v 111.0.5500.0 (arm64)](https://github.com/lexesv/chromium-macos-proprietary-codecs/releases/download/v111/Chromium.app.zip)

If you zip, upload Chromium.app to some web service and download it to an Arm Mac, browsers will set the com.apple.quarantine bit, which will cause the Finder to say "Chromium" is damanged and can't be opened. You should move it to the Trash.". In Console.app, the kernel will log kernel: Security policy would not allow process: 2204, /Users/you/Downloads/Chromium.app/Contents/MacOS/Chromium and amfid will log amfid: /Users/you/Downloads/Chromium.app/Contents/MacOS/Chromium signature not valid: -67050. 

To fix this, open a terminal and run:

```
xattr -rc Chromium.app
```
