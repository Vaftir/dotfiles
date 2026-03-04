# LazyVim Keymaps

## Leader Keys

- `<leader>` = `Space`
- `<localleader>` = `\`

## General

| Key | Description | Mode |
|-----|-------------|------|
| `j` | Down | n, x |
| `k` | Up | n, x |
| `Ctrl+h` | Go to Left Window | n |
| `Ctrl+j` | Go to Lower Window | n |
| `Ctrl+k` | Go to Upper Window | n |
| `Ctrl+l` | Go to Right Window | n |

## Files

| Key | Description |
|-----|-------------|
| `<leader>ff` | Find files |
| `<leader>fr` | Recent files |
| `<leader>fb` | Buffers |
| `<leader>fg` | Live grep |
| `<leader>fw` | Grep word |
| `<leader>fc` | Find config |
| `<leader>fn` | New file |

## Search & Replace

| Key | Description |
|-----|-------------|
| `<leader>sr` | Search and Replace (Grug-Far) |

## Buffers

| Key | Description |
|-----|-------------|
| `[b` | Previous buffer |
| `]b` | Next buffer |
| `<leader>bb` | Switch to other buffer |
| `<leader>bd` | Delete buffer |
| `<leader>bD` | Delete buffer (force) |

## Windows

| Key | Description |
|-----|-------------|
| `<leader>ww` | Other window |
| `<leader>wd` | Delete window |
| `<leader>w-` | Split window below |
| `<leader>w\|` | Split window right |
| `<leader>-` | Split window below |
| `<leader>\|` | Split window right |

## Tabs

| Key | Description |
|-----|-------------|
| `<leader><tab>l` | Last tab |
| `<leader><tab>f` | First tab |
| `<leader><tab><tab>` | New tab |
| `<leader><tab>]` | Next tab |
| `<leader><tab>d` | Close tab |

## LSP

| Key | Description |
|-----|-------------|
| `gd` | Go to definition |
| `gD` | Go to declaration |
| `gr` | References |
| `gI` | Implementation |
| `gy` | Type definition |
| `K` | Hover documentation |
| `gK` | Signature help |
| `<leader>ca` | Code action |
| `<leader>cA` | Source action |
| `<leader>cr` | Rename |
| `<leader>cD` | Type definition (floating) |

## Git

| Key | Description |
|-----|-------------|
| `<leader>gg` | Lazygit |
| `<leader>gG` | Lazygit (cwd) |
| `<leader>gb` | Git blame |
| `<leader>gf` | Git diff file |
| `<leader>gd` | Git diff hunk |
| `<leader>gp` | Git preview hunk |
| `<leader>gb` | Git blame |
| `<leader>gs` | Git status |
| `<leader>gS` | Git status (cwd) |

## Diagnostics

| Key | Description |
|-----|-------------|
| `[d` | Previous diagnostic |
| `]d` | Next diagnostic |
| `<leader>cd` | Line diagnostics |
| `<leader>cq` | Diagnostic quickfix |
| `<leader>xl` | Location list |
| `<leader>xq` | Quickfix list |

## Terminal

| Key | Description |
|-----|-------------|
| `<c-/>` | Terminal (horizontal) |
| `<c-_>` | Terminal (horizontal) |
| `<c-\>` | Terminal (vertical) |
| `<leader>ft` | Toggle float term |
| `Esc Esc` | Hide terminal |

## Todo Comments

| Key | Description |
|-----|-------------|
| `[t` | Previous todo |
| `]t` | Next todo |
| `<leader>st` | Todo search |
| `<leader>sT` | Todo Telescope |
| `<leader>xt` | Todo trouble |
| `<leader>xT` | Todo trouble / |

## Neovim Navigation (tmux)

| Key | Description |
|-----|-------------|
| `Ctrl+h` | Navigate left (Neovim/tmux) |
| `Ctrl+j` | Navigate down (Neovim/tmux) |
| `Ctrl+k` | Navigate up (Neovim/tmux) |
| `Ctrl+l` | Navigate right (Neovim/tmux) |

**Note**: These work seamlessly with tmux panes when using the nvim-tmux-navigation plugin.

## Custom Commands

| Command | Description |
|----------|-------------|
| `:Lazy` | Open Lazy |
| `:Mason` | Open Mason |
| `:Telescope` | Open Telescope |
| `:GrugFar` | Open search & replace |

## Movement

| Key | Description |
|-----|-------------|
| `h/j/k/l` | Move left/down/up/right |
| `w/W` | Next/previous word |
| `e/E` | End of word |
| `b/B` | Beginning of word |
| `0` | Beginning of line |
| `$` | End of line |
| `^` | First non-blank character |
| `gg` | First line |
| `G` | Last line |

## Editing

| Key | Description |
|-----|-------------|
| `i` | Insert mode |
| `a` | Append |
| `I/A` | Insert at beginning/end of line |
| `o/O` | New line below/above |
| `x` | Delete character |
| `dd` | Delete line |
| `yy` | Yank line |
| `p` | Paste |
| `u` | Undo |
| `Ctrl+r` | Redo |
| `.` | Repeat last command |
| `r` | Replace character |
| `R` | Replace mode |
| `~` | Toggle case |
| `>>` | Indent line |
| `<<` | Unindent line |
| `==` | Auto indent |

## Visual Mode

| Key | Description |
|-----|-------------|
| `v` | Visual character |
| `V` | Visual line |
| `Ctrl+v` | Visual block |
| `o` | Move to other end |
| `aw` | Select a word |
| `ab` | Select a block |
| `ib` | Select inner block |
| `at` | Select a tag |
| `it` | Select inner tag |
