# LBB Builder Theme

A colorful VS Code/VSCodium theme for builders. Balanced contrast, calm surfaces, and a matching terminal palette help you stay comfortable during long coding sessions.

## Features

- Dark and light variants: "LBB Builder Dark" and "LBB Builder Light"
- Comfortable contrast for long sessions without sacrificing clarity
- Integrated terminal colors included automatically via the theme ANSI palette

## Install

### VSCodium (Open VSX)

1. Open Extensions
2. Search for "LBB Builder Theme"
3. Install and reload

### VS Code (Marketplace or VSIX)

Marketplace:
1. Open Extensions
2. Search for "LBB Builder Theme"
3. Install and reload

VSIX:
1. Download the `.vsix`
2. In VS Code, open Extensions and choose "Install from VSIX..."
3. Select the file and reload

## Activate the theme

Use the Command Palette and run "Preferences: Color Theme", then choose:
- LBB Builder Dark
- LBB Builder Light

## Integrated terminal

The integrated terminal picks up the theme's ANSI palette automatically. No extra configuration is required.

## External terminal (macOS Terminal.app)

Terminal.app can render selection colors that look washed out with custom palettes. A quick fix:

1. Terminal.app > Settings > Profiles > your profile > Text
2. Set "Selection color" to `#6E6A86`
3. Set "Selected text color" to `#ECEFF4` (or white)

## Starship prompt (recommended)

Starship is a fast, cross-platform prompt that works the same on macOS, Linux, and Windows.

### Install Starship

macOS (install script):
```
curl -sS https://starship.rs/install.sh | sh
```

macOS (Homebrew, optional):
```
brew install starship
```

Windows (winget):
```
winget install --id Starship.Starship
```

Linux (install script):
```
curl -sS https://starship.rs/install.sh | sh
```

### Enable Starship

zsh (`~/.zshrc`):
```
eval "$(starship init zsh)"
```

bash (`~/.bashrc` or `~/.bash_profile`):
```
eval "$(starship init bash)"
```

PowerShell (`$PROFILE`):
```
Invoke-Expression (&starship init powershell)
```

If you already set a custom prompt (for example `PROMPT`, `PS1`, or `ZSH_THEME`), remove or comment it out so Starship can take over.

### Apply the LBB Builder preset

Copy the preset into Starship's config path:

macOS/Linux:
```
cp extras/starship/starship.toml ~/.config/starship.toml
```

Windows (PowerShell):
```
Copy-Item extras\starship\starship.toml "$env:USERPROFILE\.config\starship.toml" -Force
```

The preset keeps the prompt clean by showing username, hostname, directory, and git branch only.
