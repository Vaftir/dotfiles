# Configuration

## Neovim (LazyVim)

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

## Git

**Location**: `git/.gitconfig`

```ini
[user]
  name = Yago Faria
  email = yagoassisfaria@gmail.com
[init]
  defaultBranch = main
```

## Starship

**Location**: `starship/.config/starship.toml`

**Theme**: Nord palette with language indicators

**Features**:
- Directory truncation
- Git branch and status
- Python, Lua, Node.js, Go, Haskell, Rust, Ruby versions
- AWS, Docker contexts
- Command duration

## Bash

**Location**: `bash/.bashrc`

**Includes**:
- fnm (Node.js version manager)
- Homebrew (Linux)
- Starship prompt
- Auto-start tmux
- PATH management

## Zsh

**Location**: `zsh/.zshrc`

**Includes**:
- fnm (Node.js version manager)
- Starship prompt
- Auto-start tmux
- History settings
- Completion

## Fish

**Location**: `fish/.config/fish/`

**Includes**:
- Custom scripts in `conf.d/`

## tmux

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

## Kitty

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
