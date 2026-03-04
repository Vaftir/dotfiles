# tmux Keymaps

## Prefix

Default prefix: `Ctrl+b`

## Custom Keybindings

| Key | Description |
|-----|-------------|
| `Ctrl+b r` | Reload config |
| `Ctrl+b \|` | Split window horizontally |
| `Ctrl+b -` | Split window vertically |

## Session Management

| Key | Description |
|-----|-------------|
| `Ctrl+b ?` | List all key bindings |
| `Ctrl+b :` | Enter command mode |
| `Ctrl+b $` | Rename session |
| `Ctrl+b d` | Detach from session |
| `Ctrl+b s` | Show session list |
| `Ctrl+b (` | Previous session |
| `Ctrl+b )` | Next session |

## Window Management

| Key | Description |
|-----|-------------|
| `Ctrl+b c` | Create new window |
| `Ctrl+b 0-9` | Select window by number |
| `Ctrl+b ,` | Rename window |
| `Ctrl+b w` | Show window list |
| `Ctrl+b &` | Kill window |
| `Ctrl+b n` | Next window |
| `Ctrl+b p` | Previous window |

## Pane Management

| Key | Description |
|-----|-------------|
| `Ctrl+b %` | Split pane vertically |
| `Ctrl+b "` | Split pane horizontally |
| `Ctrl+b ←` | Navigate to left pane |
| `Ctrl+b →` | Navigate to right pane |
| `Ctrl+b ↑` | Navigate to upper pane |
| `Ctrl+b ↓` | Navigate to lower pane |
| `Ctrl+b o` | Swap panes |
| `Ctrl+b x` | Kill pane |
| `Ctrl+b z` | Toggle zoom |

## Layouts

| Key | Description |
|-----|-------------|
| `Ctrl+b Space` | Switch layouts (even horizontal, even vertical, main horizontal, main vertical, tiled) |

## Copy Mode

| Key | Description |
|-----|-------------|
| `Ctrl+b [` | Enter copy mode |
| `q` | Exit copy mode |
| `Space` | Start selection |
| `Enter` | Copy selection |
| `]` | Paste from buffer |

## CLI Commands

| Command | Description |
|---------|-------------|
| `tmux` | Start new session |
| `tmux new -s name` | Start named session |
| `tmux ls` | List all sessions |
| `tmux attach` | Attach to last session |
| `tmux attach -t name` | Attach to named session |
| `tmux kill-session -t name` | Kill named session |
| `tmux source-file ~/.tmux.conf` | Reload config |
| `tmux list-keys` | List all key bindings |

## Neovim Navigation (Seamless)

| Key | Description |
|-----|-------------|
| `Ctrl+h` | Navigate left (Neovim/tmux) |
| `Ctrl+j` | Navigate down (Neovim/tmux) |
| `Ctrl+k` | Navigate up (Neovim/tmux) |
| `Ctrl+l` | Navigate right (Neovim/tmux) |
| `Ctrl+\` | Navigate last pane |

**Note**: These work seamlessly between Neovim splits and tmux panes when using the nvim-tmux-navigation plugin.
