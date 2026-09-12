# wallpapers

Personal wallpaper collection. Used as a git submodule in my dotfiles.

## Layout

The `theme` switcher picks a random image from the directory named by the active
theme's `WALLPAPER_DIR` (see `dotfiles/themes/<name>/theme.env`). A directory name
is therefore a *pointer target*, not necessarily a theme name — several themes can
and do share one directory.

| Directory | Contents |
|---|---|
| `everforest/` | Muted greens and greys — pairs with the dark everforest theme. |
| `light/` | Bright, high-key images. Shared by every light theme (`everforest-light`, `tokyonight-day`, `dawnfox`, `dayfox`). |
| `neutral/` | Theme-agnostic darks — city, ocean, space. Shared by the dark tokyonight and nightfox themes, and the **fallback** when a theme's directory is missing or empty. |
| `wanderers/` | A coherent 37-image set, not theme-specific. Not used by the switcher. |

Give a theme its own directory when you have images that genuinely only suit it;
otherwise point `WALLPAPER_DIR` at `light` or `neutral`. The switcher only looks one
level deep and only at `*.jpg` / `*.jpeg` / `*.png`.
