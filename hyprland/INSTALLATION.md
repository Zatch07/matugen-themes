# Hyprland & Hyprlock Matugen Guide

This folder contains the templates to sync your Hyprland borders and Hyprlock screen with your wallpaper colors.

## 📁 Files
1. `colors.conf`: Main Hyprland color configuration.
2. `hyprlock-colors.conf`: Colors for the hyprlock screen.

## 🚀 How to Implement

### Step 1: Copy Files
Copy these files to your Matugen templates folder:
`~/.config/matugen/templates/hyprland/`

### Step 2: Configure Matugen
Add these sections to your `~/.config/matugen/config.toml`:

```toml
[templates.hyprland]
input_path = '~/.config/matugen/templates/hyprland/colors.conf'
output_path = '~/.config/hypr/hyprland/colors.conf'

[templates.hyprlock]
input_path = '~/.config/matugen/templates/hyprland/hyprlock-colors.conf'
output_path = '~/.config/hypr/hyprlock/colors.conf'
```

### Step 3: Source in Hyprland
Ensure your `hyprland.conf` sources the generated file:
\`\`\`conf
source = ~/.config/hypr/hyprland/colors.conf
\`\`\`

---
**Tip**: This setup ensures that your window borders and lock screen always match your active wallpaper.
