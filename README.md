# LinuxToys
A collection of tools for Linux in a user-friendly way.

![LinuxToys](https://github.com/psygreg/linuxtoys/blob/8836d345c41cf867e0d26aeb6cb88baf78835e5a/src/scrnshot.png)

## Compatibility

LinuxToys and it's features' compatibility is only *guaranteed* on the operating systems explicitly mentioned in the **Usage** section. Your mileage may vary in operating systems derivated from those, and I'll gladly accept contributions to get it running in more systems. It isn't compatible, *and never will be*, with immutable distributions, since the whole point of LinuxToys is to make changes to the host OS. 

## Usage
- Install the proper package for your operating system from [Releases](https://github.com/psygreg/linuxtoys/releases) and run it from the applications menu or use it directly from source.

### Standalone
Paste the command into your terminal to get the script from the source, in Arch Linux you will need to install `libnewt` to run the script.

#### Stable branch
```bash
curl -fsSL https://raw.githubusercontent.com/psygreg/linuxtoys/main/src/linuxtoys.sh | bash
```

### Ubuntu (latest and latest LTS releases)
There's a PPA available for LinuxToys. To use it:
`sudo add-apt-repository ppa:psygreg/linuxtoys &&
sudo apt update`

### Debian
Use the **.deb** package provided in [Releases](https://github.com/psygreg/linuxtoys/releases).

### Fedora, OpenSUSE, AlmaLinux and RHEL
You may obtain it and keep it up-to-date from the COPR repository: `sudo dnf copr enable psygreg/linuxtoys`

### Arch Linux
Get it from the [Arch User Repository](https://aur.archlinux.org/packages/linuxtoys-bin) using `aura -A linuxtoys-bin`; or

- Download the PKGBUILD and `.install` files from [Releases](https://github.com/psygreg/linuxtoys/releases)
- Run `makepkg -si` on the folder you downloaded the file to install.

## Limitations
- **Shader Booster** only works in systems using the `bash` or `zsh` shells as default. 
- **GRUB-btrfs**, besides its obvious requirements, depends on `systemd-init` to enable boot snapshots and cleanup.
- **Lucidglyph** is only confirmed to work on **Gnome** and **Plasma** desktops. With all others, your mileage may vary.
- The **linux-cachyos** kernel port to Debian/Ubuntu-based systems may require its **LTO** setting changed to 'Full' or 'None' to work in some systems. *ThinLTO is only known to work in the standard Ubuntu-Gnome flavour and in Debian Testing, so far, although it is the optimal setting if it works for your system.*
- **LACT** is an overclocking tool. Use with caution.
- **PyEnv** only supports running in `bash` or `zsh` shells.
- **Godot 4 .NET** a.k.a. *GodotSharp* is not compatible with Arch-based operating systems, as there isn't a .NET SDK available from Microsoft officially for those.
- **Unity Hub** only supports **Debian**, **Ubuntu** and **Red Hat Enterprise Linux**, so its installer will only work on these systems.

## Building from source
### .deb package
This will require `debuild`, obtained from the `devscripts` package..

- Clone the repo.
- Open terminal on `src/buildfiles/deb/linuxtoys*`
- Run `debuild -S` for .changes file or `debuild -us -uc` for a .deb package.

### .rpm package
Requires `rpmbuild`.

- Clone the repo.
- Open terminal on the `src/buildfiles/rpm/rpmbuild` subdirectory.
- `rpmbuild -bb SPECS/linuxtoys.spec`

## Contributing

To contribute with translations, you can fork this repo, add a new language file to the `resources/lang` folder and send a Pull Request. I can make the necessary adjustments to the program's code myself to accomodate new languages.

Other contributions can be made by forking, adding your changes and sending a Pull Request as well.

**All Pull Requests will be manually checked before approval.**

## Credits

- [Lucidglyph](https://github.com/maximilionus/lucidglyph/tree/v0.11.0) by **Maximilionus**
- [GRUB-btrfs](https://github.com/Antynea/grub-btrfs) by **Antynea**
- [Pipewire Audio Capture plugin for OBS Studio](https://github.com/dimtpap/obs-pipewire-audio-capture) by **Dimitris Papaioanou**
- [LACT](https://github.com/ilya-zlobintsev/LACT) by **Ilya Zlobintsev**
- [Easy Effects](https://github.com/wwmm/easyeffects) by **Wellington Wallace**
- [StreamController](https://github.com/StreamController/StreamController) by **'Core447'**
- [MakeResolveDeb](https://www.danieltufvesson.com/makeresolvedeb) by **Daniel Tufvesson**
- [DaVinciBox](https://github.com/zelikos/davincibox) by **Patrick Csikos**
- [Darktable](https://www.darktable.org)
- [Foliate](https://johnfactotum.github.io/foliate) by **John Factotum**
- [Custom Wine Builds](https://github.com/NelloKudo/WineBuilder) by **'NelloKudo'**
- [LSFG-VK](https://github.com/PancakeTAS/lsfg-vk) by **'PancakeTAS'**
- [auto-cpufreq](https://github.com/AdnanHodzic/auto-cpufreq) by **Adnan Hodzic**
- [Touchégg](https://github.com/JoseExposito/touchegg) by **José Expósito**
- [Vinegar](https://vinegarhq.org/Home/index.html) by **the VinegarHQ team**
- [Chaotic AUR](https://aur.chaotic.cx/)
- [The CachyOS Team](https://github.com/CachyOS/linux-cachyos)
- [Pyenv](https://github.com/pyenv)
- [NVM-sh](https://github.com/nvm-sh)
- [WiVRn](https://github.com/WiVRn)
- [Oversteer](https://github.com/berarma/oversteer) by **Bernat**
- [WinApps](https://github.com/winapps-org/winapps)
- And the Linux Community
