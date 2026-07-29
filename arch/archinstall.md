# Arch Linux Install Guide
- This guide is intended for new Linux users who want to install Arch Linux using the `archinstall` helper, which simplifies the installation process.
- Before following this guide, I highly recommend reading the resources listed below. I guarantee they will save you time and a lot of frustration later on.

## Info

[![Arch](https://img.shields.io/badge/Arch-Linux-1793D1?style=for-the-badge&logo=arch-linux&logoColor=white)](https://archlinux.org/)
[![Guide](https://img.shields.io/badge/Install-Guide-0F172A?style=for-the-badge&logo=github&logoColor=white)](https://github.com/)
[![ISO](https://img.shields.io/badge/ISO-2026.07.01--x86__64-4C1?style=for-the-badge)]()
[![Archinstall](https://img.shields.io/badge/Archinstall-4.4-2D7DD2?style=for-the-badge)]()

## Resources
- [Arch Installation Guide](https://wiki.archlinux.org/title/Installation_guide)
- [Archinstall](https://wiki.archlinux.org/title/Archinstall)
- [File Systems](https://wiki.archlinux.org/title/File_systems)

## 1. Connect to the network

- Use `iwctl` for wireless setup.
- Run `ip address` to confirm the machine received an IP address.
- Run `ping 8.8.8.8` to verify WAN access.

## 2. Start the installer

- Launch the installation process with `archinstall`.

## 3. archinstall settings

### Language and locale

- Leave language and locale values at their defaults.

### Mirrors and repositories

- Choose your region for mirrors.
- Add optional repositories if needed.
- Use `/` to search.
- Example: type `/Canada` and press `Enter`.
- Enable `multilib` if you want Steam or other gaming packages.

### Disk configuration

- Use the default partition layout as a best-effort setup.

Recommended filesystems:

- `btrfs`: fast, supports snapshots, and works well for desktop installs.
- `ext4`: stable and familiar.
- `xfs`: useful for larger storage pools or NAS-style setups.
- `f2fs`: best suited for flash storage.

My preference is `btrfs` with subvolumes and compression enabled.
- Snapshot tools: `Snapper` and `Timeshift` are both good.

### Swap

- Leave swap at the default setting.

### Bootloader

- Keep the default `GRUB` bootloader.

### Kernel choice

- `linux`: standard stable kernel.
- `linux-zen`: good for gaming or heavier workloads.
- `linux-lts`: better for long-term stability.

### Hostname

- Set a hostname that matches the machine.

### Authentication

- Set the root password.
- Create your user account.

### Profile and desktop environment

- `KDE Plasma`: familiar and Windows-like.
- `Hyprland`: a strong Wayland option when paired with Noctalia Shell.
- `Niri`: my current preference with DankMaterial.

### Graphics driver

- Choose the correct driver for your GPU.

### Greeter

- I use `SDDM` with a custom theme from GitHub.

### Applications and services

- Bluetooth support
- Audio through PipeWire
- Firewall with `ufw`
- Additional fonts: `noto-fonts`

### Network configuration

- I usually use `NetworkManager`, but it can be buggy.
- If needed, try the ISO defaults or another network option.

### Additional packages

- `vscode`
- `git`
- `steam`
- `spotify`
- `brave`
- `firefox`
- `openrgb`
- `cursor`
- `nvim`

### Timezone

- Search for your timezone and select it.

## 4. Finish installation

- Run the installation.
- Reboot when it completes.
