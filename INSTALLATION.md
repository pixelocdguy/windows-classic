# Required

The Windows Classic Theme can be configured to look like Windows XP - Windows Classic, Windows 2000 or Windows Mellenium Edition. Where differences exist, they will be noted below.

## Initial Installation of Files

### Window Manager

#### Openbox

Copy `openbox/windows-classic/` folder from this repository to `~/.themes/`

*or*

#### KWin

Run the following terminal command (Debian/Lubuntu/etc.):

`sudo apt install kwin-x11 systemsettings5 --no-install-suggests --no-install-recommends`

#### Desktop Environment - LXQt

Copy the `lxqt/windows-classic/` folder contents from this repository to `~/.local/share/lxqt/themes/windows-classic/`

Install your favorite Icons Theme from another source. *This is currently out of scope of this project.*

Copy the Tahoma Font file/s from your Windows installation at
`C:\Windows\Fonts\tahoma.ttf & tahomabd.ttf` and
`C:\Windows\Fonts\tahomabd.ttf`
to
`~/.fonts/`

Rebuild font cache by running the following command (Debian/Lubuntu/etc.):
`fc-cache -fv`

Install your favorite Cursor Theme from another source. *This is currently out of scope of this project.*

## Configuration of Appearance

### Widget Style

Open LXQt Configuration Center
Open the Appearance applet

Click Widget Style if not already active

Set the following:

#### Qt Style: Windows

#### Qt Pallette
- **Window:** Red: 212, Green: 208, Blue: 200
- **Selection:** Red: 10, Green: 36, Blue: 106
- **Visited Link:** Red: 128, Green: 0, Blue: 128

### Icons Theme

Click Icons Style

Select your preferred Windows XP or 2k/ME icon theme

### LXQt Theme

Click LXQt

Select Windows-classic

### Font

Set the following:

#### Font
- **Font name:** Tahoma
- **Style:** Normal
- **Point size:** 8

### Cursor

Click Cursor

Select your preferred Windows XP or 2k/ME cursor theme

**Click Apply > Close**

# Recommended

## Configuration of the Desktop

Desktop Preferences > Background > Select background color > Red: 58, Green: 110, 165 & Wallpaper image file: null > OK
General > Icons > Icon size: 32 x 32
Label Text > Select font: Tahoma, Regular, 8pt
NOT XP - Select shadow color: #3a6ea5 (this mimics no shadow like Win2k/ME).
Advanced > Uncheck Home, Check Trash, Computer, Network
Move Web Browser shortcut to desktop from Extras folder
Copy (not Move - as we need this elsewhere as well) Documents shortcut to desktop from Extras folder
Re-arrange to the following order at the top left: My Documents, Computer, Network, Trash, Web Browser

## Configuration of the Panel

Remove Desktop Switcher, Quick Launch, System Tray (this has been replaced by the Status Notifier in LXQt), Show Desktop

World clock > Display format > Check Use 12-hour format
General > Show tooltip

## Configuration of the Start Menu

Application menu > General - Check Button text (The actual text should be set to 'Start' by the theme QSS file, but you can change this if you desire here)

Move Extras/Applications/ folder to ~/.local/share/

Menu file: Set via Desktop Settings > Menu File
Set Menu file to "~/.local/share/lxqt/themes/windpos-classic/extras/lxqt-applications.menu

# Optional

## KWin Title Font Size Fix

*Note - if you do this, you'll have to use the qt5 app to configure various settings rather than the build in LXQt app.*

Install qt5ct via your distro's package manager

Add following session variable via LXQt > Session Config > Advanced
QT_QPA_PLATFORMTHEME=qt5ct
