# To be update in 2025

# System Preferences

First thing you need to do, on any OS actually, is update the system! For that: **App Store application > Updates.**
Also upgrade your OS incase you want to work on the latest OS. Sierra is a free upgrade so please check that.

If this is a new computer, there are a couple tweaks you would like to make to the System Preferences. Feel free to follow these, or to ignore them, depending on your personal preferences.

### General
- Appearance->Graphite
- Highlight color:->Blue
- Sidebar icon size->Medium
- Show scroll Bars->When scrolling
- Click on the scroll bar to:->Jump to the spot that's cliked
- Default Web Browser->Firefox when it will have been installed
- Allow Handoff between this Mac and your iCloud devices->Unchecked
- Use LCD font smoothing when available->Checked

### Desktop and Screen Saver
#### Desktop
- Apple->Solid Colors->Solid Gray Medium

#### Screen Saver
- Screen Saver->Message
- Start After->5 minutes
- Hot Corners...->Top Left=Start Screen Saver

### Dock
- Size:->closer to the small side
- Position on screen->Left
- Minimize windows using:->Genie effect
- Prefer tabs when opening documents:->In Full Screen Only
- Double-click a window's title bar to->Zoom
- Minimize window into application icon->Checked
- Animate opening applications->Unchecked
- Automatically hide and show the Dock->Unchecked
- Show indicators for open applications->Checked

### Mission Control
- Keep default preferences

### Language & Region
- Preferred languages
  - English - primary
  - Français
- Region->France
- First day of week->Monday
- Calendar->Gregorian
- Time format: 24-Hour Time
- Temperature:->°C-Celsius
- List sort order:->Universal

### Security & Privacy
A development machine should be secured against threads as well as any other machine \(or even _especially_ a development machine\). Therefore we should install

* a virus scanner,
* a firewall, and
* disk encryption.

#### General
- Require password immediately after sleep or screen saver begins
- Disable automatic login->Checked
- Allow apps dowloaded from:->App Store and identified developers

#### Virus scanner

Head over to [Avira](https://www.avira.com/), download and install their latest free package.

#### Firewall

This one is a bit controversial. If you do not install software which allows network access of any kind, skip it. If you run potentially vulnerable software you don't want to be accessed from other machines, consider turning the built-in firewall on. This particularly applies if you develop network software.

To turn the built-in firewall on:

1. Choose Apple menu \(\) &gt; System Preferences, then click Security & Privacy.
2. Click the Firewall tab.
3. Click the Lock button, then enter an administrator name and password.
4. Click Turn On Firewall.
5. Click Firewall Options.
6. Uncheck 'Automatically allow signed software to receive incoming connections'.
7. Enable stealth mode

The step 6 disables automatic access for software from the App Store. From now on you can either add \(dis\)allowed programs to the list within the Firewall Options or just click on Allow\/Deny, if you get a popup asking you if a specific software may be accessed.

#### Disk Encryption

Another controversial point. If you have a desktop machine in a secured building, you probably do not need disk encryption. If you travel a lot and take your notebook with you \(including all your source codes\), you should perhaps travel with disk encryption enabled. I cannot tell the impact of disk encryption on system performance because I never used my MacBook unencrypted.

The following steps were taken from the [official apple support page](https://support.apple.com/en-us/HT204837) on this:

1. Choose Apple menu \(\) &gt; System Preferences, then click Security & Privacy.
2. Click the FileVault tab.
3. Click the Lock button, then enter an administrator name and password.
4. Click Turn On FileVault.
5. Follow the instructions. In my opinion you should create a local and offline possibility to disable encryption, when you are asked how to regain access in case of anything.

#### Privacy
- Enable location services->Unchecked
- Diagnostic & Usage->Unchecked

#### Advanced
Require an administrator password to access system-wide preferences->Checked

### Spotlight
- Uncheck fonts, images, files etc.
- Uncheck the keyboard shortcuts as we'll be replacing them with Alfred.

### Displays
- Resolution->Scaled
- Airplay Display:->Off

### Energy Saver
- Turn display off after:->5 minutes
- Put hard disks to sleep when possible->Checked
- Slightly dim the display when on battery power->Checked
- Enable Power Nap while on battery power->Unchecked
- Show battery status in menu bar->Unchecked (we'll replace it by iStat)

### Trackpad
- Point & Click
    - Lookup and data detectors->Checked
    - Secondary click->Checked
    - Tap to click->Unchecked
    - Click->Medium
    - Tracking speed->fourth mark
    - Silent clicking->Unchecked
    - Force click and haptic feedback->Checked
- Scroll and Zoom
    - Check all
- More gestures
  - Check all

### iCloud
- Add an iCloud account and sync iCloud drive, Photos, Calendar, Find my mac, Contacts etc.

### App Store
- Automatically check for updates->Checked
  - All sub-options are Unchecked
- Password settings:->Always Require & Require Password

### Bluetooth
Check how to disable "discoverable"

### Sharing
- No sharing checked

### Users and Groups
- Turn off Guest User
- Create an Admin profile
- Create a standard user profile with no rights to administer
- Login Options-> Change fast switching user menu to Icon
- Set up Password, Apple id, Picture , etc.
- Login Options
  - Automatic login:->Unchecked
  - Display login window as:->Name and password
  - Show the Sleep, Restart and Shutdown buttons->Checked
  - Show input menu in login window->Unchecked
  - Show password hints->Unchecked
  - Show fast user switching menu as->Full Name
  - User voiceOver in the login window->Unchecked

### Siri
  - Enable Siri->Unchecked

### Finder
- Toolbar
    - Update to add path, new folder and delete
- Sidebar
    - Add home and code directory
    - Remove shared and tags
    - New finder window to open in the home directory
