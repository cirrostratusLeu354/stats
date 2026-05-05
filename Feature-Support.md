## Features

- **Non-Blocking Architecture** Engineered in Go with asynchronous concurrency. Data synchronization occurs entirely in the background, ensuring zero latency impact on the editor's performance.
- **Privacy-Centric** Storage Data is persisted exclusively to your personal MongoDB instance. This self-hosted model ensures complete data ownership with no third-party tracking, telemetry, or subscription fees.
- **Automated Dependency Management** The plugin automatically detects the host operating system (Linux/macOS) and retrieves the appropriate pre-compiled binary during the initial setup.
- **Portfolio Visualization** Includes a dedicated CLI utility for generating high-resolution statistical charts, optimized for seamless integration into GitHub Profile READMEs.
- **Granular Telemetry** Intelligently tracks and categorizes development activity by project, programming language, and file type without requiring manual configuration.

---

## Editor Compatibility & Features

TakaTime is built to be cross-platform and editor-agnostic. Both plugins share the same core Go binaries, ensuring a consistent experience.

| Feature | Neovim | VS Code | Antigravity | OS Support |
| :--- | :--- | :--- | :--- | :--- |
| **Background Uploader** | ✓ Supported | ✓ Supported |✓ Supported | Windows, macOS, Linux |
| **Interactive Dashboard** | ✓ Supported | ✓ Supported | ✓ Supported | Windows, macOS, Linux |
| **Profile Stats Reporter** | ✓ Supported | ✓ Supported |✓ Supported | Windows, macOS, Linux |
| **Privacy Controls** | ✓ Supported (`.takaignore`, `.takatrack`) | ⚙ Planned (Future Release) |⚙ Planned (Future Release) | All OS |

*(Note: Privacy controls for VS Code and Antigravity are currently in active development and will be rolling out soon!)*

