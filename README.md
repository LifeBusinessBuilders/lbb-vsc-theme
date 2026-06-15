# LBB Builder Theme

A colorful VS Code/VSCodium theme pack for builders — vivid where your eye glances, calm where it lingers, with a matching integrated-terminal palette for long coding sessions.

**Three themes, pick the one that fits your light:**
- **LBB Builder Dark** — the calm default; rich color on a soft, tinted dark background.
- **LBB Builder Light** — built independently for bright rooms and daylight (not an inverted dark theme).
- **LBB Builder Aurora** — vivid, higher-saturation, deeper background for when you want more energy.

Every color is derived in the perceptual OKLCH space and checked against APCA contrast targets, so accents stay legible and prose stays comfortable over long sessions. See the design notes for the research behind it.

---

## Install

- **VS Code (Marketplace):** Extensions → search **LBB Builder Theme** → Install.
- **VSCodium (Open VSX):** Extensions → search **LBB Builder Theme** → Install.
- **From a VSIX (anywhere):** download from [Releases](https://github.com/LifeBusinessBuilders/lbb-vsc-theme/releases) (or build one — see below), then Extensions → `…` → **Install from VSIX…**.

Links: [Website](https://lifebusinessbuilders.com/) · [Open VSX](https://open-vsx.org/extension/lifebusinessbuilders/lbb-vsc-theme) · [Marketplace](https://marketplace.visualstudio.com/items?itemName=lifebusinessbuilders.lbb-vsc-theme) · [GitHub](https://github.com/LifeBusinessBuilders/lbb-vsc-theme)

---

## Activate

Command Palette → **Preferences: Color Theme** → pick **LBB Builder Dark**, **Light**, or **Aurora**.

---

## Integrated terminal

The integrated terminal picks up each theme's ANSI palette automatically — nothing to configure.

---

## Colorful `ls` in your terminal (Linux/macOS)

The colors of **folders and files in `ls` output** don't come from your editor theme — they come from your shell's `LS_COLORS`, and a system update can quietly switch them off. To turn them back on, add this to `~/.bashrc` (or `~/.zshrc`):

```sh
alias ls='ls --color=auto'
eval "$(dircolors -b ~/.config/lbb/dircolors 2>/dev/null || dircolors -b)"
```

This repo ships an optional preset at **`extras/dircolors/lbb.dircolors`** — copy it to `~/.config/lbb/dircolors` and the snippet above will load it (it falls back to sensible defaults if the file isn't there). It uses the standard 16 ANSI colors, so it automatically matches whichever LBB terminal theme is active.

---

## Going further (optional)

### Starship prompt
[Starship](https://starship.rs) is a fast cross-shell prompt. It styles your **prompt** (`user@host:path`), not your file colors. Install it, then add `eval "$(starship init bash)"` (or `zsh`/`powershell`) to your shell config. A minimal LBB preset lives at `extras/starship/starship.toml` — copy it to `~/.config/starship.toml`.

### External terminals
Want matching colors outside VS Code? Import the schemes in `extras/`:
- **Windows Terminal:** `extras/windows-terminal/schemes.json` · **iTerm2:** `extras/iterm2/*.itermcolors`

---

## Build a VSIX

```sh
npm i && npx vsce package --no-dependencies
```

## License

MIT — see [LICENSE](LICENSE).
