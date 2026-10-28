# pi-lazygit

Lightweight Pi extension that opens [lazygit](https://github.com/jesseduffield/lazygit) in a popup terminal.

Based on `pi-lazygit` by Neil Vallecer ([Neil-urk12/pi-dots](https://github.com/Neil-urk12/pi-dots)), MIT.

## Install

```bash
pi install git:github.com/aburneikis/pi-lazygit
```

## Usage

| Method | Action |
|--------|--------|
| `/lazygit` | Command palette |
| `Ctrl+Shift+G` | Keyboard shortcut |

Opens lazygit fullscreen in the current repo. Returns to pi when you quit (`q`).

## Requirements

- [lazygit](https://github.com/jesseduffield/lazygit#installation) installed and on `PATH`
- Pi running in TUI mode

## How it works

Stops the TUI, spawns lazygit with inherited stdio (fullscreen takeover), then restarts the TUI on exit. Uses async `spawn` so the TUI event loop stays unblocked.
