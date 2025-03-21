> [!WARNING] 
>All of these commands are designed for Ubuntu. Check out the [UMU Git Repo](https://github.com/Open-Wine-Components/umu-launcher?tab=readme-ov-file#building) for other destro support and the [Gio website](https://gioui.org/doc/install/linux) for Dependencies. Also, If Your using vinegar from the flatpak then you must make sure the config is clear by default, but in this case we are using Vingar from the source so we will have to configure it ourselves.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <h1 align="center">
        <img src="https://github.com/Nightro-Fx/Vinegar-Guide/blob/main/img/Vinegar.png" width="40" alt="Logo"/> 
        Vinegar Studio Installation Guide
    </h1>
</html>

#### ❤️ Acknowledgements  
Massive shoutout to the [Official Vinegar Discord Server](https://discord.gg/vinegarhq-1069506340973707304) for providing me the resources and the information needed to make this guide possible.

###### Delete your previous Vinegar from flatpak
```bash
flatpak uninstall --delete-data org.vinegarhq.Vinegar -y
```
###### Installing Required Dependencies
```bash
sudo apt install gcc pkg-config libwayland-dev libx11-dev libx11-xcb-dev libxkbcommon-x11-dev libgles2-mesa-dev libegl1-mesa-dev libffi-dev libxcursor-dev libvulkan-dev
sudo dpkg --add-architecture i386 && sudo apt update
sudo apt install python3-xlib python3-filelock apparmor-profiles libgl1-mesa-dri:i386 libglx-mesa0:i386
```

###### Getting the latest version of Golang. [Chick Here](https://github.com/Nightro-Fx/Golang-Installation-Guide) to see a guide!
```bash
# Make sure you have the 1.23.3 version (latest). If you don't, then check out the link above.
go version
```

###### Installting Vinegar from Source
```bash
cd
sudo apt-get install git
git clone https://github.com/vinegarhq/vinegar
cd vinegar
sudo apt-get install make
sudo make install
sudo make mime
```
###### Make sure Vinegar is installed
```bash
vinegar version
```

###### Installing UMU
```bash
cd
wget https://github.com/Open-Wine-Components/umu-launcher/releases/download/1.2.5/python3-umu-launcher_1.2.5-1_amd64_ubuntu-noble.deb -O umu-launcher.deb && \
sudo dpkg -i umu-launcher.deb && \
sudo apt-get install -f  # Fix dependencies if needed
```

###### Editing Vinegar Config File
```bash
vinegar edit
```
###### Configure your file to look something like this
```bash
[studio]
wineroot = "/home/Nightro-Fx/.local/share/Steam/compatibilitytools.d/GE-Proton9-26"

[studio.env]
PROTONPATH = "/home/Nightro-Fx/.local/share/Steam/compatibilitytools.d/GE-Proton9-26"
GAMEID= "0"
PROTON_VERB = "run"
```

###### Opening Vinergar :)
```bash
WINEPREFIX="~/.local/share/vinegar/prefixes/studio" GAMEID=0 PROTONPATH=GE-Proton umu-run "$(find ~/.local/share/vinegar/versions/ -name "RobloxStudioBeta.exe")"
```

###### Import File Location
Your sandboxed environment for the Vinegar is located at `~/.var/app/org.vinegarhq.Vinegar/data/vinegar/prefixes/studio/drive_c`. 
Run the following command to open the directory:
```bash
xdg-open ~/.var/app/org.vinegarhq.Vinegar/data/vinegar/prefixes/studio/drive_c
```

## Troubleshooting
#### Black Login Window
<img src="https://github.com/Nightro-Fx/Vinegar-Guide/blob/main/img/Black_Login_Window.png" width="600" alt="Problem"/> 

###### To fix the black login window run:
```bash
pkill -f webview
```

###### Now MAKE SURE to have Chrome installed and set as your default browser, When you press *Login via Browser*. You need to login from Chrome

#### Dependencies Issues
<img src="https://github.com/Nightro-Fx/Vinegar-Guide/blob/main/img/Neofetch.png" width="400" alt="Problem"/> 

```bash
# Please upgrade your Ubuntu to the latest version (24.04 LTS), Umu Launcher is NOT made for older versions
xdg-open https://youtu.be/ULeBDYl6uJM?si=OYYzdfMykdl0HAWm
```
