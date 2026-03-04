# Troubleshooting

## Symlink Conflicts

If stow reports conflicts, backup existing files:

```bash
mv ~/.existing-file ~/.existing-file.backup
stow <module>
```

## tmux Not Working

Check tmux version:

```bash
tmux -V  # Should be 3.2a+
```

Reload tmux config:

```bash
tmux source-file ~/.tmux.conf
```

## Neovim Plugins Not Loading

Open Neovim and run:

```vim
:Lazy sync
```

## Kitty Transparency Not Working

If transparency doesn't work on macOS:
- Make sure you're not using the Wayland backend
- Check if `background_opacity` is set in `kitty.conf`

## tmux Navigation Not Working

Ensure both Neovim and tmux are configured:
1. Check Neovim plugin: `nvim-tmux-navigation` is installed
2. Check tmux config: Vim detection is configured in `.tmux.conf`
3. Restart tmux: `tmux kill-server`
