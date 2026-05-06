# VS Code Matugen Implementation Guide

This folder contains the two files needed to enable dynamic, instant-update theming in VS Code.

## 📁 Files
1. `dankshell.json`: The base theme file.
2. `vscode-premium.json.tpl`: The settings template (for instant color updates).

## 🚀 How to Implement

### Step 1: Copy Files
Copy both files into your Matugen templates directory:
`~/.config/matugen/templates/vscode/`

### Step 2: Configure Matugen
Add these two sections to your `~/.config/matugen/config.toml`:

```toml
[templates.vscode]
input_path = '~/.config/matugen/templates/vscode/dankshell.json'
output_path = '~/.vscode/extensions/matugen-theme/themes/matugen-color-theme.json'

[templates.vscode_settings]
input_path = '~/.config/matugen/templates/vscode/vscode-premium.json.tpl'
output_path = '~/.config/Code/User/settings.json'
```

### Step 3: Set VS Code Theme
1. Open VS Code.
2. Press `Ctrl + Shift + P` and type **"Color Theme"**.
3. Select **"Matugen Dynamic Theme"**.

### Step 4: Apply Wallpaper
Run Matugen with any image to generate and apply the colors:
```bash
matugen image /path/to/wallpaper.png
```

---
**Note**: The settings file (`vscode-premium.json.tpl`) is what allows the colors to update **instantly** without reloading VS Code.
