
## Installation
Welcome to the TakaTime setup guide! This page covers everything you need to get the time tracker installed and running seamlessly in your environment. Below, you will find step-by-step installation instructions for VS Code, Neovim, and Google Antigravity, followed by a complete guide on how to configure your own free, self-hosted MongoDB database to keep your coding telemetry 100% private.

### Using VS Code 

https://github.com/user-attachments/assets/a3c492d8-898c-497a-bc0c-c2f8ebc5d03b

---

### Using [lazy.nvim](https://github.com/folke/lazy.nvim)

https://github.com/user-attachments/assets/edf09531-ed66-4709-9b78-5edc90843510



Add this to your plugin configuration:

```lua
return {
  "Rtarun3606k/TakaTime",
  lazy = false,
  config = function()
    -- Optional: Enable debug mode if you run into issues
    require("taka-time").setup({
        debug = false
    })
  end,
}
```

---

### Using Antigravity
https://github.com/user-attachments/assets/da108968-c204-486b-9969-bf5ff24b0835


###  How to Install Manually (Using `.vsix`)
1. **Download the file:** [Click here to download takatime-0.1.1.vsix](https://github.com/Rtarun3606k/TakaTime/releases/download/v2.2.2/takatime-0.1.1.vsix) directly.
3. **Install from VSIX:** Click the **...** (three dots/gear icon) at the top right of the Extensions panel and select **"Install from VSIX..."**.
4. **Select the file:** Locate and select the `.vsix` file you just downloaded.
5. **Configure Database:** Once installed, run the `TakaTime: Setup` command (or click the status bar) and enter your MongoDB Connection String.



---

##  Setup Guide

- ### Step 1: Get a Database

  You need a MongoDB connection string. You have two free options:
  - add all ip access `(if you want github Stats its required)`
  - <img width="986" height="752" alt="image" src="https://github.com/user-attachments/assets/d9433977-e841-4e0d-a1d2-9847901501d6" />
  - Cloud (Recommended): Create a free account on MongoDB Atlas. Create a free cluster and get your connection string (e.g., mongodb+srv://user:pass@cluster...).
  - Local (Docker): Run docker run -d -p 27017:27017 mongo.
  
- ### Step 2: Initialize the Plugin
  
  Open Neovim.
  
  Run the setup command:
  Vim Script
  
  ```nvim
  :TakaInit
  ```
  
  Paste your MongoDB Connection String when prompted. (This is saved securely in your local data folder, ~/.local/share/nvim/taka_data.json).
  
- ### Step 3: Verify

  Run the status command to check if everything is working:
  Vim Script
  
  ```nvim
  :TakaStatus
  ```
  
  If it says "TakaTime is configured and running," you are good to go!

- ### Step 4: Interactive Dashboard (New!)

TakaTime now includes a fully interactive, terminal-based dashboard directly inside your editor. View your coding stats, language breakdowns, and project times without ever leaving your workflow or opening a browser.

How to open the dashboard:

VS Code: Click the Graph Icon in the top-right corner of your editor tab, or use the Command Palette (Ctrl+Shift+P / Cmd+Shift+P) and run TakaTime: Open Dashboard.

- #### Neovim: Run the command :TakaDash to open the floating UI.
    ```nvim
    :TakaDashboard
    ```
- #### VsCode :
  <img width="1093" height="110" alt="image" src="https://github.com/user-attachments/assets/b65ebbef-993f-4368-951e-fb6c1c4bd952" />

  
