
Unlock your device's full potential!

Sparserestore works on all versions iOS 17.0-17.7 and iOS 18.0-18.1 beta 4. There is partial support for iOS 17.7.1 and iOS 18.1b5-18.2 beta 2.

iOS 18.2 developer beta 3 (public beta 2) and newer is not supported.

Make sure you have installed the requirements if you are on Windows or Linux.

This uses the sparserestore exploit to write to files outside of the intended restore location, like mobilegestalt. Read the Getting the File section to learn how to get your mobilegestalt file.

Note: I am not responsible if your device bootloops. Please back up your data before using!

Features
iOS 17.0+
Enable Dynamic Island on any device
Enable iPhone X gestures on iPhone SEs
Change Device Model Name (ie what shows in the Settings app)
Enable Boot Chime
Enable Charge Limit
Enable Tap to Wake on unsupported devices (ie iPhone SEs)
Enable Collision SOS
Enable Stage Manager
Disable the Wallpaper Parallax
Disable Region Restrictions (ie. Shutter Sound)
Note: This does not include enabling EU sideloading outside the EU. That will come later.
Show the Apple Pencil options in Settings app
Show the Action Button options in Settings app
Show Internal Storage info (Might cause problems on some devices, use at your own risk)
EU Enabler (iOS 17.6-)
Springboard Options (from Cowabunga Lite)
Set Lock Screen Footnote
Disable Lock After Respring
Disable Screen Dimming While Charging
Disable Low Battery Alerts
Internal Options (from Cowabunga Lite)
Build Version in Status Bar
Force Right to Left
Force Metal HUD Debug
iMessage Diagnostics
IDS Diagnostics
VC Diagnostics
App Store Debug Gesture
Notes App Debug Mode
Disable Daemons:
OTAd
UsageTrackingAgent
Game Center
Screen Time Agent
Logs, Dumps, and Crash Reports
ATWAKEUP
Tipsd
VPN
Chinese WLAN service
HealthKit
Risky (Hidden) Options:
Disable thermalmonitord
OTA Killer
Custom Resolution
iOS 18.0+
Enable iPhone 16 camera button page in the Settings app
Enable AOD & AOD Vibrancy on any device
Feature Flags (iOS 18.1b4-):
Enabling lock screen clock animation, lock screen page duplication button, and more!
Disabling the new iOS 18 Photos UI (iOS 18.0 betas only, unknown which patched it)
iOS 18.1+
AI Enabler + Device Spoofing (fixed in iOS 18.2db3)
Requirements:
Windows:

Either Apple Devices (from Microsoft Store) app or iTunes (from Apple website)
Linux:

usbmuxd and libimobiledevice
For Running Python:

pymobiledevice3
PySide6
Python 3.8 or newer
Running the Python Program
Note: It is highly recommended to use a virtual environment:

python3 -m venv .env # only needed once
# macOS/Linux:  source .env/bin/activate
# Windows:      .env/Scripts/activate.bat
pip3 install -r requirements.txt # only needed once
python3 main_app.py
Note: It may be either python/pip or python3/pip3 depending on your path.

The CLI version can be ran with python3 cli_app.py.

Getting the File
You need to get the mobilegestalt file that is specific to your device. To do that, follow these steps:

Install the Shortcuts app from the iOS app store.
Download this shortcut: https://www.icloud.com/shortcuts/d6f0a136ddda4714a80750512911c53b
Save the file and share it to your computer.
Place it in the same folder as the python file (or specify the path in the program)
Building
To compile mainwindow.ui for Python, run the following command: pyside6-uic qt/mainwindow.ui -o qt/ui_mainwindow.py

To compile the resources file for Python, run the following command: pyside6-rcc qt/resources.qrc -o resources_rc.py

The application itself can be compiled by running compile.py.


Credits
LeminLimez for Nugget
JJTech for Sparserestore/TrollRestore
disfordottie for some global flag features
Mikasa-san for Quiet Daemon
sneakyf1shy for AI Eligibility (iOS 18.1 beta 4 and below)
lrdsnow for EU Enabler
pymobiledevice3 for restoring and device algorithms.
PySide6 for the GUI library.
