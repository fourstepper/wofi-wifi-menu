# wofi-wifi-menu

A wifi menu primarily designed for use with Sway. Uses wofi and nmcli

### Dependencies

* nmcli (networkmanager)
* iw
* wofi
* bash

### Installation

* make sure you have all the dependencies installed

* run the following commands in your terminal. Replace initial directory with a
directory of personal choice

```
cd DESIRED_DIRECTORY
git clone https://github.com/fourstepper/wofi-wifi-menu.git
cd wofi-wifi-menu
bash "./wofi-wifi-menu.sh"
```

#### Arch Linux

There's also an AUR package available for Arch Linux. You can install it using [yay](https://github.com/Jguer/yay)
or by using the makepkg utility.

```bash
#install package from AUR
yay -S wofi-wifi-menu-git

#copy default config
cp /usr/share/wofi/wifi.example ~/.config/wofi/wifi

#run wofi-wifi-menu
wofi-wifi-menu
```


### Configuration

wofi-wifi-menu has an example configuration file in the repository. It will run
without it, but will warn you if it does not exist.

To configure wofi-wifi-menu, first cd into the directory it is installed into.
Then edit the file `config.example`.
It should contain the following variables:

* position
* y-offset
* x-offset
* fields

#### position

position can be configured where the number represents the position on this
screen in this way

| *Screen*   | Left | Right | Center |
|------------|------|-------|--------|
| **Top**    | 1    | 2     | 3      |
| **Center** | 8    | 0     | 4      |
| **Bottom** | 7    | 6     | 5      |

#### y-offset

y-offset is measured in pixels. A positive value moves the window downward,
while a negative value moves it upward.

#### x-offset

x-offset is measured in pixels. A positive value move the window rightward, while
a negative value moves it leftward.

#### fields

fields choose what is displayed by the menu. The available fields are as follows:

`NAME,SSID,SSID-HEX,BSSID,MODE,CHAN,FREQ,RATE,SIGNAL,BARS,SECURITY,WPA-FLAGS,RSN-FLAGS,DEVICE,ACTIVE,IN-USE,DBUS-PATH`
