---
title: "Install OpenBangla Keyboard"
date: 2020-09-23+06:00
draft: false
description: "Install OpenBangla Keyboard"
---

**If you had installed OpenBangla Keyboard 1.5.1 or earlier version, [please uninstall it first.](https://github.com/OpenBangla/OpenBangla-Keyboard/wiki/Uninstalling-OpenBangla-Keyboard)**

First set up our repositories for your distro, then you can install normally with your package manager.

## Ubuntu & derivatives
Run these commands to set up our repository:

**Note: Don't forget to run `source /etc/os-release`, otherwise the installation will fail.**
```bash
source /etc/os-release
sudo sh -c "wget https://dl.bintray.com/openbangla/i/pub.key -q -O - | apt-key add -"
sudo sh -c "wget https://dl.bintray.com/openbangla/i/ubuntu.conf -q -O - | sed s/@NAME@/$UBUNTU_CODENAME/ > /etc/apt/sources.list.d/openbangla.list"
sudo apt update
sudo apt install openbangla-keyboard
```

## Debian
Run these commands to set up our repository:

**Note: Don't forget to run `source /etc/os-release`, otherwise the installation will fail.**
```bash
source /etc/os-release
sudo sh -c "wget https://dl.bintray.com/openbangla/i/pub.key -q -O - | apt-key add -"
sudo sh -c "wget https://dl.bintray.com/openbangla/i/debian.conf  -q -O - | sed s/@NAME@/$VERSION_CODENAME/ > /etc/apt/sources.list.d/openbangla.list"
sudo apt update
sudo apt install openbangla-keyboard
```

## Fedora
Run these commands to set up our repository:
```bash
sudo rpm --import https://dl.bintray.com/openbangla/i/pub.key
sudo sh -c "curl https://dl.bintray.com/openbangla/i/fedora.conf > /etc/yum.repos.d/openbangla.repo"
sudo dnf install openbangla-keyboard
```

## Archlinux
Run these commands to set up our repository:
```bash
sudo sh -c "curl https://dl.bintray.com/openbangla/i/pub.key | pacman-key -a -"
sudo pacman-key --lsign-key "openbanglateam@gmail.com"
sudo sh -c "curl https://dl.bintray.com/openbangla/i/archlinux.conf >> /etc/pacman.conf"
sudo pacman -Syy
sudo pacman -S openbangla-keyboard
```

## Others
You can also install by downloading necessary packages from our [Releases](https://github.com/OpenBangla/OpenBangla-Keyboard/releases) page.

## Finally
After you have installed OpenBangla Keyboard, you may need to [configure your desktop environment](https://github.com/OpenBangla/OpenBangla-Keyboard/wiki/Configuring-Environment).

If this does not work out for you, please create an [Issue](https://github.com/OpenBangla/OpenBangla-Keyboard/issues).

