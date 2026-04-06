# Dotfiles for Omarchy

Personal configuration files for [Omarchy](https://omarchy.org/) (Arch Linux + Hyprland).

## Management

This repository is managed by [GNU Stow](https://www.gnu.org/software/stow/). It uses symbolic links to map files from this repository to your home directory (`~`).

### Repository Structure

- `dot-config/`: Contains all user personalizations for Omarchy components:
  - `hypr/`: Hyprland configuration (window rules, monitor aliases, workspace bindings).
  - `waybar/`: Status bar configuration.
  - `omarchy/`: Custom themes (`gruvu`, `pandora`) and automation hooks.
  - `walker/`, `mako/`, `swayosd/`: App launcher, notification daemon, and OSD configs.
- `dot-zshrc`: Zsh shell configuration.
- `dot-mise.toml`: [mise](https://github.com/jdx/mise) tool version management.
- `scripts/`: Helper scripts for initial environment setup.

## Features & Customizations

### Monitor & Workspace Layout
The configuration is optimized for a 3-monitor setup using hardware-specific descriptions:
- **Center (`$predator`)**: Acer X34 GS (DP-1). Workspaces 1-8.
- **Left (`$benq_left`)**: BenQ EX2780Q (DP-3). Workspace 9.
- **Right (`$benq_right`)**: BenQ EX2780Q (DP-2). Workspace 10.

### Window Rules
- **Steam**: Forced to tile by default (overriding standard Omarchy floating behavior).
- **Discord/Spotify**: Automatically moved to Workspace 9 (Left Monitor).

### Automation
- **Post-Update Hook**: A custom hook at `~/.config/omarchy/hooks/post-update` automatically runs `stow` after every system update to ensure symbolic links remain intact.

## Setup & Usage

### 1. Requirements
Ensure the following tools are installed:
- [GNU Stow](https://www.gnu.org/software/stow/)
- [FZF](https://github.com/junegunn/fzf)
- [mise-en-place](https://github.com/jdx/mise)

### 2. Linking Dotfiles
Clone this repository and run the following command to link your configurations:
```bash
stow --dotfiles -v -d ~/proj/dotfiles -t ~ .
```

### 3. Additional Steps
- **Fonts**: Run `scripts/download_nerd_fonts.sh` to install Fira Code Nerd Font.
- **Tools**: Run `mise install` to install managed tools (like `zoxide`).

## Maintenance

After making local configuration changes, remember to commit and push:
```bash
git add .
git commit -m "Update settings"
git push origin main
```
