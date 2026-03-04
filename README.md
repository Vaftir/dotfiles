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

## Dotfiles Philosophy

### Two Common Approaches

There are two main philosophies for managing dotfiles:

#### 1. **Declarative Dotfiles** (Common Approach)
- Only configuration files are versioned
- User installs tools manually before applying configs
- Documentation explains prerequisites
- ✅ More flexible and portable across systems
- ✅ Safer (doesn't install things without permission)
- ❌ Requires manual setup of dependencies

#### 2. **Automated Setup Scripts** (Your Case)
- Installation script automates dependency installation
- Applies configurations automatically
- ✅ One-shot: run one script and you're ready
- ✅ Less chance of human error
- ❌ Less flexible (may install unwanted things)
- ❌ More complex to maintain

### This Repository: Hybrid Approach

**Recommended approach** - Separates concerns:
- `dotfiles/` - Configuration files only (this repo)
- `setup.sh` (optional) - Automated installation script

```bash
#!/bin/bash
# setup.sh - Optional automated installation

# Install dependencies
brew install stow tmux neovim
curl -sS https://starship.rs/install.sh | sh

# Clone and apply configs
cd ~
git clone git@github.com:Vaftir/dotfiles.git ~/.dotfiles
cd ~/.dotfiles
stow nvim git starship bash fish zsh tmux kitty
```

### Individual Module Install

Install only the configurations you need:

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

### Remove Symlinks

To remove symlinks for a specific module:

```bash
cd ~/.dotfiles
stow -D <module>
```

## Configuration

### Neovim (LazyVim)

**Location**: `nvim/.config/nvim/`

**Plugins**:
- `blink.cmp` - Fast autocompletion
- `nvim-treesitter` - Syntax highlighting
- `mason.nvim` - LSP server management
- `gitsigns.nvim` - Git integration
- `grug-far.nvim` - Find and replace
- `lualine.nvim` - Status line
- `catppuccin` / `tokyonight` - Color schemes
- `nvim-tmux-navigation` - Seamless tmux-Neovim navigation

**Keybindings**:
- `gd` - Go to definition
- `K` - Hover documentation
- `<leader>ff` - Find files
- `<leader>fg` - Live grep
- `Ctrl+h/j/k/l` - Navigate between Neovim splits and tmux panes

### Git

**Location**: `git/.gitconfig`

```ini
[user]
  name = Yago Faria
  email = yagoassisfaria@gmail.com
[init]
  defaultBranch = main
```

### Starship

**Location**: `starship/.config/starship.toml`

**Theme**: Nord palette with language indicators

**Features**:
- Directory truncation
- Git branch and status
- Python, Lua, Node.js, Go, Haskell, Rust, Ruby versions
- AWS, Docker contexts
- Command duration

### Bash

**Location**: `bash/.bashrc`

**Includes**:
- fnm (Node.js version manager)
- Homebrew (Linux)
- Starship prompt
- Auto-start tmux
- PATH management

### Zsh

**Location**: `zsh/.zshrc`

**Includes**:
- fnm (Node.js version manager)
- Starship prompt
- Auto-start tmux
- History settings
- Completion

### Fish

**Location**: `fish/.config/fish/`

**Includes**:
- Custom scripts in `conf.d/`

### tmux

**Location**: `tmux/.tmux.conf`

**Features**:
- Base index starts at 1
- Nord color scheme
- Custom keybindings:
  - `Ctrl+b r` - Reload config
  - `Ctrl+b |` - Split horizontal
  - `Ctrl+b -` - Split vertical
- Seamless navigation with Neovim (`Ctrl+h/j/k/l`)

**Status Bar**:
- Bottom positioned
- Nord colors (#2E3440, #D8DEE9, #5E81AC)

### Kitty

**Location**: `kitty/.config/kitty/kitty.conf`

**Features**:
- Nord color scheme
- JetBrains Mono Nerd Font
- Transparency (85% opacity, adjustable)
- Tab bar with powerline style
- Auto-start tmux
- Window padding

**Transparency Controls**:
- `Ctrl+Shift+F11` - Decrease transparency
- `Ctrl+Shift+F12` - Increase transparency

## Maintenance

### Update Dotfiles

```bash
cd ~/.dotfiles
git pull
```

### Add New Configuration

```bash
# Add file to existing module
cp ~/.new-config ~/.dotfiles/<module>/.config/

# Commit changes
cd ~/.dotfiles
git add .
git commit -m "Add new configuration"
git push
```

### Install Missing Dependencies

```bash
# Install GNU Stow
brew install stow

# Install Starship
curl -sS https://starship.rs/install.sh | sh

# Install fnm
curl -fsSL https://fnm.vercel.app/install | bash

# Install tmux
brew install tmux

# Install Kitty (macOS)
brew install --cask kitty

# Install Kitty (Linux)
# See: https://sw.kovidgoyal.net/kitty/binary/
```

## Troubleshooting

### Symlink Conflicts

If stow reports conflicts, backup existing files:

```bash
mv ~/.existing-file ~/.existing-file.backup
stow <module>
```

### tmux Not Working

Check tmux version:

```bash
tmux -V  # Should be 3.2a+
```

Reload tmux config:

```bash
tmux source-file ~/.tmux.conf
```

### Neovim Plugins Not Loading

Open Neovim and run:

```vim
:Lazy sync
```

### Kitty Transparency Not Working

If transparency doesn't work on macOS:
- Make sure you're not using the Wayland backend
- Check if `background_opacity` is set in `kitty.conf`

### tmux Navigation Not Working

Ensure both Neovim and tmux are configured:
1. Check Neovim plugin: `nvim-tmux-navigation` is installed
2. Check tmux config: Vim detection is configured in `.tmux.conf`
3. Restart tmux: `tmux kill-server`

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
