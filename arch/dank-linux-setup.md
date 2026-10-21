# Dank Linux Setup Guide

This guide helps new Niri / Dank Linux users configure a comfortable desktop environment. It focuses on visual polish, fonts, common apps, and basic system tweaks. Read the linked resources first — they'll save time and frustration.

## Info

[![Arch](https://img.shields.io/badge/Arch-Linux-0F172A?style=for-the-badge&logo=arch-linux)](https://archlinux.org/)
[![Guide](https://img.shields.io/badge/Setup-Guide-0F172A?style=for-the-badge&logo=github)](https://github.com/)
[![Niri](https://img.shields.io/badge/niri-Dank_Linux-0F172A?style=for-the-badge&logo=niri)](https://github.com/niri-wm/niri)

## Resources

- Niri documentation: https://niri-wm.github.io/niri/index.html
- Dank Linux docs: https://danklinux.com/docs/

## Prerequisites

- A running Arch-based system (or compatible) with a Wayland session.
- Basic familiarity with Pacman and editing dotfiles.
- Optional: `yay` or another AUR helper for Nerd fonts and community packages.

## Quick package recommendations

- Display / shell: `niri`, `niri-dank-material` (if available)
- Fonts: `noto-fonts`, `ttf-roboto-mono-nerd`, `ttf-fira-code-nerd`
- Audio: PipeWire (`pipewire`, `pipewire-pulse`)
- Networking: `networkmanager` or ISO defaults
- Utilities: `git`, `vscode`, `openrgb`, `steam` (optional)

Install example (use `sudo` and adjust for your package manager):

```bash
sudo pacman -S noto-fonts
# If using an AUR helper for Nerd fonts:
yay -S ttf-roboto-mono-nerd ttf-fira-code-nerd
```

## 1. Avatars and wallpapers

- Create organized folders: `~/Pictures/avatars` and `~/Pictures/wallpapers`.
- Sources: Wallhaven (https://wallhaven.cc), 4k-wallpapers (https://4kwallpapers.com), game screenshots, or personal art.
- Choose a theme and set Automatic Cycling with a comfortable interval.
- Set the system theme to Auto so accent and wallpaper behavior stay consistent.

Tips:
- Keep wallpapers scaled and cropped to your monitor resolution to avoid pixelation.

## 2. Fonts and typography

- Pick a UI font and a monospace for terminals/editors. I use RobotoMono Nerd Font for UI and Fira Code for code.
- Search available packages: `pacman -Ss noto-fonts` or `pacman -Ss ttf`.
- Install example:

```bash
sudo pacman -S ttf-roboto-mono-nerd
sudo pacman -S ttf-fira-code-nerd
```

Configure font settings in the Appearance panel or your `~/.config/niri/config` if you prefer dotfile control.

## 3. Enable Weather widget

- Enable the weather widget in the Dank Bar settings.
- Set a custom location (city name or coordinates) and preferred units (C/F).

## 4. Configure the Dank Bar

- Open Appearance → Settings and adjust:
	- Opacity
	- Spacing
	- Visibility (auto-hide, always-on)
- Add widgets: system tray, network, battery, weather, workspace indicator, and a quick-launch area.

## 5. Default applications & autostart

- Set your default browser, terminal, editor, and media player in the Default Apps panel.
- Add autostart entries for apps you want at login (e.g., `steam`, `openrgb`, compositor helpers).

## 6. System, power & security

- Review Power settings and set suspend, brightness, and lid behavior to your preference.
- Enable a firewall (e.g., `ufw`) for desktop safety: `sudo pacman -S ufw` then `sudo systemctl enable --now ufw`.
- Use PipeWire for audio and enable Bluetooth support if needed.

## 7. Troubleshooting & tips

- If fonts look wrong, clear font cache: `fc-cache -f -v` and restart your session.
- If widgets misbehave, try resetting the bar configuration or checking `~/.config/niri/` for user overrides.

## Closing notes

This guide is a concise checklist to get a polished Dank Linux desktop. For deeper customization, consult the Niri and Dank Linux docs linked above.
