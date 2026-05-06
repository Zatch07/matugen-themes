# KDE Plasma Matugen Guide

This template allows you to sync KDE Plasma color schemes with your Matugen generated colors.

## 📁 Files
1. `color.txt`: The Plasma color scheme template.

## 🚀 How to Implement

### Step 1: Copy File
Copy the template to your Matugen templates folder:
`~/.config/matugen/templates/kde/`

### Step 2: Configure Matugen
Add this section to your `~/.config/matugen/config.toml`:

```toml
[templates.kde_colors]
input_path = '~/.config/matugen/templates/kde/color.txt'
output_path = '~/.local/state/quickshell/user/generated/color.txt'
```

---
**Note**: This is designed to be used with the Quickshell system to dynamically apply the generated color scheme to your Plasma desktop environment.
