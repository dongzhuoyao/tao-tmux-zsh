# Tao's Tmux & ZSH Configuration

Personal dotfiles for tmux and zsh.

## ZSH Configuration

- **Framework**: [Oh My Zsh](https://ohmyz.sh/) with `robbyrussell` theme
- **Plugins**: `git`
- **PATH additions**: `~/.local/bin`, `~/.opencode/bin`
- **Conda**: Miniconda3 initialization
- **Terminal**: Blinking cursor enabled (for Termius)

## Tmux Configuration

- **Theme**: Gruvbox dark (self-contained, no framework required)
- **Lines**: ~200 lines of pure tmux config

### Key Bindings

| Binding | Action |
|---------|--------|
| `C-a` | Secondary prefix (GNU Screen-compatible) |
| `h/j/k/l` | Pane navigation (vim-style) |
| `H/J/K/L` | Pane resizing |
| `-` / `_` | Split horizontal / vertical |
| `Tab` | Last window |
| `C-h` / `C-l` | Previous / next window |
| `Enter` | Copy mode |
| `v` / `C-v` / `y` | Begin selection / rectangle toggle / copy |
| `m` | Toggle mouse |
| `r` | Reload config |
| `c` | New window (retains current path) |

### Status Bar

- **Left**: Session name (yellow background)
- **Right**: Prefix indicator, time, date, username, hostname

### Features

- Gruvbox dark color scheme
- Mouse support (toggle with `prefix + m`)
- Focused pane highlighting
- Bell notifications (for Claude Code hooks)
- True color (24-bit) support
- macOS clipboard integration (`prefix + y`)
- 50K scrollback history

## Installation

```bash
# Clone this repo
git clone git@github.com:dongzhuoyao/tao-tmux-zsh.git ~/tao-tmux-zsh

# Backup existing configs
[ -f ~/.zshrc ] && mv ~/.zshrc ~/.zshrc.bak
[ -f ~/.tmux.conf ] && mv ~/.tmux.conf ~/.tmux.conf.bak

# Symlink configs
ln -sf ~/tao-tmux-zsh/zshrc ~/.zshrc
ln -sf ~/tao-tmux-zsh/tmux.conf ~/.tmux.conf

# Reload tmux (if already running)
tmux source-file ~/.tmux.conf
```

## Dependencies

- [Oh My Zsh](https://ohmyz.sh/)
- [Miniconda3](https://docs.conda.io/en/latest/miniconda.html) (optional)
- tmux 2.6+
