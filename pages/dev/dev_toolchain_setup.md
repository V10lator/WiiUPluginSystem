---
title: Setting up the toolchain
tags: [toolchain]
keywords: toolchain, devkitpro, devkitppc
last_updated: November 20, 2018
sidebar: dev_sidebar
permalink: dev_toolchain_setup.html
folder: dev
topnav: topnav
---

To compile homebrew for the Wii U, you need the [devkitPro Toolchain](https://devkitpro.org/), the offical "getting started" can be found [here](https://devkitpro.org/wiki/Getting_Started).

## Windows
On Windows you can use the [graphical installer](https://github.com/devkitPro/installer/releases) to install devkitpro.

After installing you can [open MSYS](https://devkitpro.org/wiki/Getting_Started#Windows) (Start -> devkitPro -> MSYS) and check if the needed packages are installed and on the newest version.
```
pacman -Syu devkitPPC --needed
pacman -Syu devkitARM --needed
pacman -Syu general-tools --needed
# We need xxd for building the plugin loader
pacman -Syu vim
```

Make sure the following environment variables are set:
```
DEVKITPRO=/opt/devkitpro
DEVKITARM=/opt/devkitpro/devkitARM
DEVKITPPC=/opt/devkitpro/devkitPPC
```

## Unix
The offical installation guide can be found [here](https://devkitpro.org/wiki/Getting_Started#Unix-like_platforms)

Basically you need to grab the [newest devkitpro pacman version](https://github.com/devkitPro/pacman/releases/) and install the `devkitPPC`, `devkitARM `, `general-tools` and `vim` (for `xxd`) package.

Example commands for installing:
```Bash
# Download newest deb file. (URL might be outdated in the future)
wget https://github.com/devkitPro/pacman/releases/download/devkitpro-pacman-1.0.1/devkitpro-pacman.deb -O /tmp/devkitpro-pacman.deb
# Install it
sudo dpkg -i /tmp/devkitpro-pacman.deb
# Install needed packages
sudo dkp-pacman -Syu devkitPPC --needed
sudo dkp-pacman -Syu devkitARM --needed
sudo dkp-pacman -Syu general-tools --needed
# We need xxd for building the plugin loader
pacman -Syu vim
```

After installing, make sure the following environment variables are set:
```
DEVKITPRO=/opt/devkitpro
DEVKITARM=/opt/devkitpro/devkitARM
DEVKITPPC=/opt/devkitpro/devkitPPC
```

## Pacman information

More information on how to use pacman can be found [here](https://devkitpro.org/wiki/devkitPro_pacman#Using_Pacman)

{% include links.html %}