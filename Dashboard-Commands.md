## TakaTime Dashboard & Commands

The TakaTime dashboard is a fully interactive, offline-first Terminal UI (TUI) built directly into your editor. Because it reads from your local SQLite cache, it boots up instantly without waiting on network latency.

### Opening the Dashboard

**In Neovim:**
You can open the floating terminal dashboard using either of these commands:
* `:TakaDash`
* `:TakaDashboard`

**In VS Code:**
* **UI Method:** Click the **Graph Icon** located in the top-right corner of your active editor tab.
* **Command Palette:** Press `Ctrl+Shift+P` (Windows/Linux) or `Cmd+Shift+P` (macOS), type `TakaTime: Open Dashboard`, and hit Enter.

---

### Interactive TUI Controls

Once the dashboard is open, you can use your keyboard to interact with the visualizations. *(Note: Ensure your terminal has focus to use these shortcuts).*

| Key | Action |
| :--- | :--- |
| **`s`** | Open the Theme Selector (preview and switch between 15+ built-in themes instantly) |
| **`↑` / `↓`** | Navigate through the theme list |
| **`Enter`** | Apply the highlighted theme |
| **`q`** or **`Esc`** | Close the dashboard and return to your code |

---

### Core Setup Commands

If you ever need to troubleshoot your connection or update your database credentials, use these core commands:

* **Initialize Setup:** * *Neovim:* `:TakaInit`
  * *VS Code:* `TakaTime: Setup`
  * *Description:* Prompts you to paste your MongoDB Connection String. This creates or updates your local configuration file.
* **Check Status:** * *Neovim:* `:TakaStatus`
  * *Description:* Verifies that the Go background daemon is successfully configured, running, and capturing heartbeats.