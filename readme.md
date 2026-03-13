## Management

This dotfile repository is managed by [GNU stow](https://www.gnu.org/software/stow/).

### Repository Structure

- `dot-config/`: Contains all user personalizations for Omarchy (Hyprland, Waybar, Walker, etc.).
- `dot-zshrc`: Shell configuration.
- `dot-mise.toml`: Tool versions management.
- `scripts/`: Helper scripts for environment setup.

### How to use

Run `stow --dotfiles -v -d ~/proj/dotfiles -t ~ .` from within the repo to link configurations.

### Requirements:

- [FZF](https://github.com/junegunn/fzf?tab=readme-ov-file#using-linux-package-managers)
- [mise](https://github.com/jdx/mise)
- [GNU Stow](https://www.gnu.org/software/stow/)

### Additional Setup:

Run the script `scripts/download_nerd_fonts.sh` to get the best font installed (fira code).

At this point all but [zoxide](https://github.com/ajeetdsouza/zoxide) should be installed. I like to manage this with mise. 

run `mise install` to get it downloaded.
