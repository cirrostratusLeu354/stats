## Troubleshooting

"TakaTime is not configured"

    Run :TakaInit again and ensure your URI is correct.

    Check if the secret file exists: ~/.local/share/nvim/taka_data.json.

Upload Failed / Syncing Forever

Enable debug mode in your config:

```Lua

 return {
  "Rtarun3606k/TakaTime",
  lazy = false,
  config = function()
    -- Optional: Enable debug mode if you run into issues
    require("taka-time").setup({
        debug = true
    })
  end,
}
```

Run :messages in Neovim to see the logs.

Ensure your IP address is whitelisted in MongoDB Atlas.

## Advanced Debugging (Log File)

If you are still facing issues, TakaTime maintains a persistent log file that tracks all binary operations, network requests, and errors.

Log Location:

    Linux/macOS:  ~/.takatime/debug-logs.log

    Windows:  C:\Users\<YourUser>\.takatime\debug-logs.log

Reporting an Issue: If you open a GitHub Issue, please attach this log file (or paste the last 50 lines). It helps us fix bugs 10x faster!


---

For Changes Look for `CHANGELOG.md`

---

