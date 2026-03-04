# Dotfiles

> GNU Stow-based dotfiles management for a productive development environment.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Stow](https://img.shields.io/badge/GNU%20Stow-2.4.1-orange.svg)

## Overview

This repository contains my personal dotfiles managed with GNU Stow. It provides a unified configuration for Neovim, Git, shell prompts, terminal multiplexing, and development tools. Works on both Linux and macOS.

## Features

- 🚀 **LazyVim** - Blazing fast Neovim config with 51+ plugins
- 🐟 **Bash & Zsh** - Shell configurations with fnm, brew, and starship
- 🎱 **Fish** - Shell configuration with custom scripts
- ⭐ **Starship** - Nord theme prompt with language detection
- 🪟 **tmux** - Terminal multiplexer with Nord color scheme
- 🐱 **Kitty** - Modern GPU-accelerated terminal emulator with Nord theme
- 🐈 **Tmux Navigation** - Seamless navigation between tmux panes and Neovim splits

## Folder Structure

```
.dotfiles/
├── bash/
│   └── .local/bin/
├── fish/
│   └── .config/fish/
├── git/
├── kitty/
│   └── .config/kitty/
├── nvim/
│   ├── .config/nvim/
│   ├── lua/config/
│   └── lua/plugins/
├── starship/
│   └── .config/
├── tmux/
└── zsh/
```

## Requirements

- GNU Stow
- Neovim
- Git
- tmux
- Starship (optional)
- Kitty (optional)
- fnm (optional)

## Installation

### Install all modules

```bash
# Clone the repository
cd ~
git clone git@github.com:Vaftir/dotfiles.git ~/.dotfiles

# Install all configurations
cd ~/.dotfiles
stow nvim git starship bash fish zsh tmux kitty
```

### Install individual modules

```bash
cd ~/.dotfiles

# Neovim (LazyVim)
stow nvim

# Git configuration
stow git

# Starship prompt
stow starship

# Bash shell (Linux)
stow bash

# Zsh shell (macOS)
stow zsh

# Fish shell
stow fish

# tmux
stow tmux

# Kitty terminal (macOS/Linux)
stow kitty
```

### Remove symlinks

```bash
cd ~/.dotfiles
stow -D <module>

# Examples:
stow -D nvim
stow -D git
stow -D tmux
```

## Update

```bash
cd ~/.dotfiles
git pull
```

## Documentation

- [Documentation](docs/) - Complete documentation index

## Platform-Specific Notes

### macOS

**Recommended stack**:
- Terminal: Kitty
- Shell: Zsh
- Auto-start: tmux via Kitty config

### Linux

**Recommended stack**:
- Terminal: Kitty (optional)
- Shell: Bash or Fish
- Auto-start: tmux via shell config

## License

MIT License - feel free to use and modify!

## Credits

- [LazyVim](https://github.com/LazyVim/LazyVim) - Neovim configuration
- [Starship](https://starship.rs) - Cross-shell prompt
- [tmux](https://github.com/tmux/tmux) - Terminal multiplexer
- [Kitty](https://sw.kovidgoyal.net/kitty/) - Terminal emulator
- [nvim-tmux-navigation](https://github.com/alexghergh/nvim-tmux-navigation) - Seamless navigation
- [GNU Stow](https://www.gnu.org/software/stow/) - Symlink farm manager

