---
title: "Install OpenBangla Keyboard"
date: 2021-05-01+06:00
draft: false
description: "Install OpenBangla Keyboard"
---

**If you had installed OpenBangla Keyboard 1.5.1 or earlier version, [please uninstall it first.](https://github.com/OpenBangla/OpenBangla-Keyboard/wiki/Uninstalling-OpenBangla-Keyboard)**


#### Ubuntu, Fedora and their derivatives
Open your terminal and run this command on your bash shell. NB : It has to be **BASH**, otherwise it won't work.
```bash
bash -c "$(wget -q https://raw.githubusercontent.com/OpenBangla/OpenBangla-Keyboard/master/tools/install.sh -O -)"
```

If this does not workout for you please create an [Issue](https://github.com/OpenBangla/OpenBangla-Keyboard/issues). While we look into the problem you can check the [Wiki](https://github.com/OpenBangla/OpenBangla-Keyboard/wiki/Installing-OpenBangla-Keyboard) for Distrowise/Distro-specific Install Instructions.

#### Archlinux and it's derivatives
There are two packages for OpenBangla Keyboard in the Arch User Repository(AUR). Use `openbangla-keyboard` if you want to make and install the package from source. Otherwise, use `openbangla-keyboard-bin` to use the binary package released for Arch and its derivatives by the maintainer. You can install it in one command with your favorite aur helper. Example commands for some popular tools:

##### `openbangla-keyboard`
* `$ pacaur -S openbangla-keyboard`
* `$ yay -S openbangla-keyboard`
* `$ yaourt -S openbangla-keyboard`


##### `openbangla-keyboard-bin`
* `$ pacaur -S openbangla-keyboard-bin`
* `$ yay -S openbangla-keyboard-bin`
* `$ yaourt -S openbangla-keyboard-bin`

Or install manually:
```bash
sudo pacman -S base-devel git
git clone https://aur.archlinux.org/openbangla-keyboard.git
cd openbangla-keyboard
makepkg -risc
```
We also provide a `.pkg.tar.zst` package for Arch Linux which you can easily install by following any of the above instruction for `openbangla-keyboard-bin`. If you want to install it manually, download the installation package from [releases page](https://github.com/OpenBangla/OpenBangla-Keyboard/releases) and install OpenBangla Keyboard on your system by running the following command:
```bash
$ sudo pacman -U package.pkg.tar.xz
```

## Others
You can also install by downloading necessary packages from our [Releases](https://github.com/OpenBangla/OpenBangla-Keyboard/releases) page.

## Finally
After you have installed OpenBangla Keyboard, you may need to [configure your desktop environment](https://github.com/OpenBangla/OpenBangla-Keyboard/wiki/Configuring-Environment).

If this does not work out for you, please create an [Issue](https://github.com/OpenBangla/OpenBangla-Keyboard/issues).

