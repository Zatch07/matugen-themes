# Spicetify (Spotify) Matugen Guide

This template integrates Matugen colors with your Spicetify-themed Spotify client.

## 📁 Files
1. `spotify-colors.ini`: The color configuration template for Spicetify.

## 🚀 How to Implement

### Step 1: Copy File
Copy the `.ini` file to your Matugen templates folder:
`~/.config/matugen/templates/spotify-colors.ini`

### Step 2: Configure Matugen
Add this section to your `~/.config/matugen/config.toml`. 

**Note**: This `post_hook` is "smart"—it will automatically detect if your Spicetify backup is outdated (common after updates) and fix it by running `restore backup apply` automatically if the standard apply fails.

```toml
[templates.spicetify]
input_path = '~/.config/matugen/templates/spotify-colors.ini'
output_path = '~/.config/spicetify/Themes/wal/color.ini'
post_hook = '''
if command -v spicetify >/dev/null 2>&1 && [ -d "$HOME/.config/spicetify/Themes/wal" ]; then
 	spicetify apply -n || spicetify restore backup apply
 	hyprctl dispatch sendshortcut "CTRL SHIFT, R, class:^(Spotify)$" || :
fi
'''
```

---
**Requirement**: You must have the "wal" theme (or similar) set up in Spicetify for this output path to work.
