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

###### Getting the latest version of Golang
```bash
# Make sure you have the 1.23.3 version (latest)
sudo snap install go --classic
go version
```

###### Installting Vinegar from Source
```bash
cd
git clone https://github.com/vinegarhq/vinegar
cd vinegar
sudo make install
make mime
```

###### Installing UMU
```bash
cd
wget https://github.com/Open-Wine-Components/umu-launcher/releases/download/1.1.4/Ubuntu-24.zip -O Ubuntu-24.zip && \
unzip Ubuntu-24.zip -d umu-launcher && \
cd umu-launcher && \
sudo dpkg -i *.deb
```

