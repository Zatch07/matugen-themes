# Spicetify (Spotify) Matugen Guide

This template integrates Matugen colors with your Spicetify-themed Spotify client.

## 📁 Files
1. `spotify-colors.ini`: The color configuration template for Spicetify.

## 🚀 How to Implement

### Step 1: Copy File
Copy the `.ini` file to your Matugen templates folder:
`~/.config/matugen/templates/spotify-colors.ini`

### Step 2: Configure Matugen
Add this section to your `~/.config/matugen/config.toml`. The `post_hook` ensures Spotify refreshes automatically:

```toml
[templates.spicetify]
input_path = '~/.config/matugen/templates/spotify-colors.ini'
output_path = '~/.config/spicetify/Themes/wal/color.ini'
post_hook = '''
if command -v spicetify >/dev/null 2>&1 && [ -d "$HOME/.config/spicetify/Themes/wal" ]; then
    spicetify apply -n || :
    hyprctl dispatch sendshortcut "CTRL SHIFT, R, class:^(Spotify)$" || :
fi
'''
```

---
**Requirement**: You must have the "wal" theme (or similar) set up in Spicetify for this output path to work.
