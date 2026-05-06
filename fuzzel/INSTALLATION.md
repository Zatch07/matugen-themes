# Fuzzel App Launcher Matugen Guide

This template themes the Fuzzel app launcher (wayland) to match your wallpaper colors.

## 📁 Files
1. `fuzzel_theme.ini`: The configuration template for Fuzzel.

## 🚀 How to Implement

### Step 1: Copy File
Copy the file to your Matugen templates folder:
`~/.config/matugen/templates/fuzzel/fuzzel_theme.ini`

### Step 2: Configure Matugen
Add this section to your `~/.config/matugen/config.toml`:

```toml
[templates.fuzzel]
input_path = '~/.config/matugen/templates/fuzzel/fuzzel_theme.ini'
output_path = '~/.config/fuzzel/fuzzel_theme.ini'
```

### Step 3: Run Fuzzel with Theme
You can launch fuzzel with the generated config:
\`\`\`bash
fuzzel --config ~/.config/fuzzel/fuzzel_theme.ini
\`\`\`

---
**Tip**: This template handles the background, selection, and border colors of the launcher UI.
