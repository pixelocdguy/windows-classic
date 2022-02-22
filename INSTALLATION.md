# INSTALLATION

# Required

The Windows Classic Theme can be configured to look like Windows XP - Windows Classic, Windows 2000 or Windows Mellenium Edition. Where differences exist, they will be noted below.

## Initial Installation of Files

### Window Manager

#### Openbox

Openbox is the default Window Manager for LXQt, so we just need to copy the theme.

Copy `openbox/windows-classic/` folder from this repository to `~/.themes/`

*or*

#### KWin

KWin is not included with LXQt by default, either vanilla LXQt or say, Lubuntu.

Run the following terminal command to install (Debian/Lubuntu/etc.):

`sudo apt install kwin-x11 systemsettings5 --no-install-suggests --no-install-recommends`

For other distros use your package manager as appropriate.

#### Desktop Environment - LXQt

Copy the `lxqt/windows-classic/` folder contents from this repository to `~/.local/share/lxqt/themes/windows-classic/`

Install your favorite Windows XP, or Windows 2k/ME Icons Theme from another source. *This is currently out of scope of this project.*

Copy the Tahoma Font file/s from your Windows installation at
`C:\Windows\Fonts\tahoma.ttf` and
`C:\Windows\Fonts\tahomabd.ttf`
to
`~/.fonts/`

Rebuild font cache by running the following command (Debian/Lubuntu/etc.):
`fc-cache -fv`

Install your favorite Cursor Theme from another source. A cursor theme based on Win95, 98, 2000, ME or XP 'Classic' should match. *This is currently out of scope of this project.*

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

Right Click on the Desktop, click Desktop Preferences

Set the following:

### General
#### Icons
**Icon size:** 32 x 32
#### Label Text
**Select font:** Tahoma, Regular, 8pt
*Win2k/ME only*
**Select shadow color:** #3a6ea5 (this mimics no shadow).
*XP*
No change - leave as black

### Background
#### Background
**Select background color:** Red: 58, Green: 110, 165
#### Wallpaper
**Wallpaper image file:** Blank/Empty/Nothing

### Advanced
#### Visible Shortcuts
**Home:** Unchecked
**Trash, Computer, Network:** Checked

Click OK

Move the Web Browser shortcut from `~/.local/share/lxqt/themes/windows-classic/extras/applications/web-browser.desktop` folder to the Desktop

Copy (not Move - as we need this elsewhere as well) the Documents shortcut (documents.desktop) from the Applications folder as per above to the Desktop
Re-arrange to the following order at the top left: My Documents, Computer, Network, Trash, Web Browser

## Configuration of the Panel

Right click anywhere on the taskbar, click Configure Panel

### Panel
#### Size
**Size:** 28px
**Icon size:** 16px

### Widgets

Select & Remove Desktop Switcher, Quick Launch, System Tray (this has been replaced by the Status Notifier in LXQt), Show Desktop

#### World Clock
**Display format**
Check Use 12-hour format
**General**
Check Show tooltip

Click OK to save the changes

## Configuration of the Start Menu

Right click on the Start button, click Configure Application Menu

### General

Check Button text *(The actual text should be set to 'Start' by the theme QSS file, but you can change this if you desire here)*

### Menu file

**Menu file:**
Browse to "~/.local/share/lxqt/themes/windpos-classic/extras/lxqt-applications.menu

Click Close to save the changes

Move the entire `extras/applications/` folder to `~/.local/share/`, e.g.

`~/.local/share/applications`

# Bug Fixes, Work Arounds

## KWin Title Font Size Fix

*Note - if you do this, you'll have to use the qt5ct application to configure various Qt related settings rather than the LXQt Appearance module.*

Install qt5ct via your distro's package manager

Add following session variable via LXQt Session Settings > Environment (Advanced)
`QT_QPA_PLATFORMTHEME=qt5ct`

# Limitations

### LXQt
- Icons in top level start menu are small instead of large
- Full Windows and Dialog boxes both have 2px inner borders. In actual Windows, dialog boxes only have a 1p inner border.
- The Documents sub-menu does not display shortcuts to recent documents. This is not possible in the open desktop spec. As a work around, you can add your preferred shortcuts here to applicatoins that maintain their own "Recent Documents" lists, e.g. LibreOffice.
- Start Search didn't appear in Windows until Vista. However, it is built in for LXQt. Instead, 95-XP just had the "Run..." dialog, similar to the LXQt Runner extension that can be added. However, due to the precence of the Search, it was decided to leave this out due to duplicate functionality.

### KWin
- KWin Title Font is not bold
- KWin Menu Shadows are not present (WinXP/2k only, ME has no shadow capability)

### Openbox
- Not possible to fully mimic the Windows Titlebar or Border due to limitations in the theming engine.
