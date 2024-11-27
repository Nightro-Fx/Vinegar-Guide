> [!WARNING] 
>All of these commands are designed for Ubuntu. Check out the [UMU Git Repo](https://github.com/Open-Wine-Components/umu-launcher?tab=readme-ov-file#building) for other destro support.
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
make mime
```
###### Make sure Vinegar is installed
```bash
vinegar version
```
###### Running Vinegar to install the Roblox Dependencies
```bash
vinegar -firstrun studio run
```

###### Installing UMU
```bash
cd
wget https://github.com/Open-Wine-Components/umu-launcher/releases/download/1.1.4/Ubuntu-24.zip -O Ubuntu-24.zip && \
unzip Ubuntu-24.zip -d umu-launcher && \
cd umu-launcher && \
sudo dpkg -i *.deb
```

###### Installing Proton GE (Located in Home)
```bash
wget -O ~/GE-Proton9-20.tar.gz https://github.com/GloriousEggroll/proton-ge-custom/releases/download/GE-Proton9-20/GE-Proton9-20.tar.gz && tar -xvzf ~/GE-Proton9-20.tar.gz -C ~ && rm ~/GE-Proton9-20.tar.gz
```

###### Editing Vinegar Config File
```bash
vinegar edit
```
###### Configure your file to look something like this
```bash
[studio]
wineroot = "/home/your_username/GE-Proton9-20"

[studio.env]
PROTONPATH = "/home/your_username/GE-Proton9-20"
GAMEID= "0"
PROTON_VERB = "run"
```
###### Setting a New Wine Prefix
```bash
vinegar delete
WINEPREFIX="~/.local/share/vinegar/prefixes/studio" GAMEID=0 PROTONPATH=GE-Proton umu-run "$(find ~/.local/share/vinegar/versions/ -name "RobloxStudioBeta.exe")"
```

## Troubleshooting
<img src="https://github.com/Nightro-Fx/Vinegar-Guide/blob/main/img/Black_Login_Window.png" width="600" alt="Problem"/> 

###### To fix the black login window run:
```bash
pkill -f webview
```

###### Now MAKE SURE to have Chrome installed and set as your default browser, When you press *Login via Browser*. You need to login from Chrome
