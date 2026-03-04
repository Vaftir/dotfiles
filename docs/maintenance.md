# Maintenance

## Update Dotfiles

```bash
cd ~/.dotfiles
git pull
```

## Add New Configuration

```bash
# Add file to existing module
cp ~/.new-config ~/.dotfiles/<module>/.config/

# Commit changes
cd ~/.dotfiles
git add .
git commit -m "Add new configuration"
git push
```

## Install Missing Dependencies

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
