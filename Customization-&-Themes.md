Welcome to the Customization & Themes guide! TakaTime is designed to seamlessly blend with your personal aesthetic, whether you are viewing your stats locally in the terminal or displaying them on your GitHub Profile. This page covers how to apply our 15+ pre-built color palettes (like Catppuccin, Nord, and Dracula), switch themes on the fly inside your interactive dashboard, and use advanced configuration flags to override specific hex colors for your automated weekly reports.

### Taka Report Customization & Themes

Taka-Report supports full customization through command-line flags. You can choose from pre-built themes or override specific colors to match your GitHub profile aesthetic.
    
### 1. Base Themes
Use the `-theme` flag to apply a pre-configured color palette.  
**Default:** `dark`
      
| Theme | Description |
| :--- | :--- |
| `dark` | GitHub Dark Dimmed (Default) |
| `light` | GitHub Light |
| `dracula` | Dracula Color Palette |
| `nord` | Nord Winter Color Palette |
| `gruvbox` | Gruvbox Retro |
| `monokai` | Monokai Vivid |
| `cyberpunk` | High Contrast Neon |
| `tokyonight` | Tokyo Night Deep Blue Palette |
| `everforest` | Everforest Soft Nature Theme |
| `iceberg` | Iceberg Cool Minimal Blues |
| `sunset` | Warm Sunset Gradient Colors |
| `deepocean` | Deep Ocean Dark Blue Theme |
| `midnight` | Midnight Purple Developer Theme |
| `catppuccin` | Catppuccin Mocha Pastel Palette |
| `solarized` | Solarized Dark Classic Palette |
| `onedark` | OneDark Pro VSCode Style |
| `material` | Material Dark UI Theme |
| `synthwave` | Retro Synthwave Neon Colors |
    
**Usage Example:**
```bash
./taka-report -theme nord
```

- ## Configuration Parameters

    You can pass these flags to the `taka-report` binary to control the data scope and visual style of your report.
    
    | Flag | Type | Default | Description |
    | :--- | :--- | :--- | :--- |
    | **`-days`** | `int` | `0` | **Data Scope:** No longer in use just set it to Zero 0|
    | **`-theme`** | `string` | `"dark"` | **Base Theme:** Selects a pre-configured color palette. <br>Options: `dark`, `light`, `dracula`, `nord`, `gruvbox`, `monokai`, `cyberpunk` |
    | **`-bg`** | `hex` | *Theme* | **Background:** Overrides the main card background color. |
    | **`-text`** | `hex` | *Theme* | **Primary Text:** Overrides the color of main headers and key statistics. |
    | **`-subtext`** | `hex` | *Theme* | **Secondary Text:** Overrides the color of labels, timestamps, and axis text. |
    | **`-bar-bg`** | `hex` | *Theme* | **Bar Background:** Overrides the color of the empty/unfilled portion of progress bars. |
    | **`-c1`** | `hex` | *Theme* | **Primary Accent:** Used for the highest values (e.g., "All Time" stat) and primary progress bars. |
    | **`-c2`** | `hex` | *Theme* | **Secondary Accent:** Used for medium-high values (e.g., "Last 30 Days"). |
    | **`-c3`** | `hex` | *Theme* | **Tertiary Accent:** Used for medium-low values (e.g., "Last 7 Days"). |
    | **`-c4`** | `hex` | *Theme* | **Quaternary Accent:** Used for the lowest values (e.g., "Yesterday") or distinct highlights. |
    
    > **Note:** Color overrides (like `-bg`) take precedence over the base `-theme`. You can start with `-theme dracula` and then just change the background with `-bg "#000000"`.

    Exapmle use  Neon Theme :
```bash
./taka-report -days=7 -bg "#0d1117" -text "#00FF00" -subtext "#008800" -bar-bg "#111111" -c1 "#00FF00" -c2 "#00DD00" -c3 "#00AA00" -c4 "#005500"
```
- ### Taka-Dashboard Customization & Themes
  Click S to select themes 
  <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f2bd6063-d068-45b2-8066-a0eba4844d11" />


