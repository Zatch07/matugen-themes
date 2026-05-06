# Antigravity Matugen Implementation Guide

This folder contains the files to enable the dynamic "Antigravity" theme in the Antigravity application (VS Code fork).

## 📁 Files
1. `dankshell.json`: The base theme file.
2. `antigravity-premium.json.tpl`: The settings template (for instant color updates).

## 🚀 How to Implement

### Step 1: Copy Files
Copy both files into your Matugen templates directory:
`~/.config/matugen/templates/antigravity/`

### Step 2: Configure Matugen
Add these two sections to your `~/.config/matugen/config.toml`:

```toml
[templates.antigravity]
input_path = '~/.config/matugen/templates/antigravity/dankshell.json'
output_path = '~/.antigravity/extensions/matugen-theme/themes/matugen-color-theme.json'

[templates.antigravity_settings]
input_path = '~/.config/matugen/templates/antigravity/antigravity-premium.json.tpl'
output_path = '~/.config/Antigravity/User/settings.json'
```

### Step 3: Set Antigravity Theme
1. Open Antigravity.
2. Press `Ctrl + Shift + P` and type **"Color Theme"**.
3. Select **"Matugen Dynamic Theme"**.

### Step 4: Apply Wallpaper
Run Matugen with any image to generate and apply the colors:
```bash
matugen image /path/to/wallpaper.png
```

---
**Note**: This setup is independent of your standard VS Code installation. It provides a glassy, premium look with instant color syncing.
