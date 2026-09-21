# 🚀 My Niri + Noctalia Shell Configuration

> A sleek, ultra-fast, and minimalist Wayland desktop setup powered by **[Niri](https://github.com/YaLTeR/niri)** and **[Noctalia Shell](https://docs.noctalia.dev/)** on **CachyOS / Arch Linux**.

![CachyOS](https://img.shields.io/badge/OS-CachyOS-00ffff?style=for-the-badge&logo=archlinux)
![Wayland](https://img.shields.io/badge/Compositor-Niri-purple?style=for-the-badge)
![Shell](https://img.shields.io/badge/Shell-Noctalia-blue?style=for-the-badge)
![RAM](https://img.shields.io/badge/RAM_Usage-~300MB-success?style=for-the-badge)

---

## ✨ Features & Highlights

- **📜 Infinite Scrollable Tiling:** Fluid horizontal window tiling powered by Niri.
- **🖥️ Dual Monitor Setup:**
  - **Primary:** LG UltraGear 180Hz (`HDMI-A-1` @ 1920x1080) hosting workspaces 1 through 9.
  - **Secondary:** Laptop Display (`eDP-1` @ 1920x1200) for auxiliary apps.
- **⌨️ Dual Keyboard Layout (Quick Toggle):**
  - **US International** with dead keys (`' + e = é`, `' + c = ç`) configured for *Attack Shark X68HE*.
  - **BR ABNT2** for native office keyboard layouts.
  - Toggle anytime via `Mod + Shift + K`.
- **🎯 1:1 RAW Mouse Precision:** Flat acceleration profile (`accel-profile "flat"`) with 0 acceleration.
- **🎨 Custom Aesthetic & Palette:**
  - Compact **8px gaps** and **14px rounded window corners**.
  - 3px active window borders with a vibrant Cyan-to-Purple gradient (`#00BFFF` → `#9D00FF`).
  - Smooth 200ms cubic window open/close transitions.
- **🛡️ Persistent Auth & Keyring:** Automatic D-Bus activation and GNOME Keyring background initialization for persistent logins (Antigravity IDE, VS Code, Brave).
- **⚡ Extreme Memory Efficiency:** Low idle RAM footprint (~300MB) keeping 8GB DDR5 RAM completely free for development workloads.
- **📊 Task Manager & Force Kill:**
  - `Ctrl + Shift + ESC` launches `btop` inside Kitty.
  - `Mod + Ctrl + Q` instantly force-kills (`kill -9`) stuck processes.

---

## 🎨 Apps & Ecosystem

| Component | Choice |
| :--- | :--- |
| **Terminal** | [Kitty](https://sw.kovidgoyal.net/kitty/) (Catppuccin Mocha + MesloLGS Nerd Font + Cursor Trail) |
| **Browser** | [Brave Browser](https://brave.com/) (Memory Saver enabled) |
| **Shell & Bar** | [Noctalia Shell](https://docs.noctalia.dev/) (Quickshell) |
| **Music** | `ncspot` (Spotify Rust TUI with Kitty album art) |
| **Task Manager** | `btop` |
| **File Manager** | `nautilus` |

---

## ⌨️ Keybindings Cheat Sheet

### 🪟 Windows & Navigation
| Shortcut | Action |
| :--- | :--- |
| `Mod` + `Return` | Open **Kitty Terminal** |
| `Mod` + `B` | Open **Brave Browser** |
| `Mod` + `E` | Open **Nautilus File Manager** |
| `Mod` + `Space` / `Alt` + `Space` | Open **Noctalia App Launcher** |
| `Mod` + `V` | Open **Noctalia Clipboard Manager** |
| `Mod` + `Shift` + `Q` | Open **Session / Power Menu** |
| `Mod` + `Alt` + `L` | Lock Screen |
| `Ctrl` + `Shift` + `ESC` | Open **btop Task Manager** |

### 🛠️ Window Management
| Shortcut | Action |
| :--- | :--- |
| `Mod` + `Q` / `Alt` + `Q` / `Alt` + `F4` | Close active window (graceful) |
| `Mod` + `Ctrl` + `Q` | **Force Kill active window** (`kill -9`) |
| `Mod` + `Arrows` / `Alt` + `WASD` | Focus Left / Right / Up / Down |
| `Mod` + `Ctrl` + `Arrows` | Move column Left / Right / Up / Down |
| `Mod` + `Shift` + `Arrows` | Move focus between monitors |
| `Mod` + `Shift` + `Ctrl` + `Arrows` | Move column to other monitor |
| `Mod` + `[` / `Mod` + `]` | Consume window into column / Expel window |
| `Mod` + `Ctrl` + `F` | Expand column to full width |
| `Alt` + `M` | Maximize column |
| `Mod` + `F` | Fullscreen window |

### ⌨️ Layout & Screenshots
| Shortcut | Action |
| :--- | :--- |
| `Mod` + `Shift` + `K` | **Toggle Keyboard Layout** (US Intl ↔ BR ABNT2) |
| `PrintScreen` / `Ctrl` + `Shift` + `1` | Interactive Screenshot (Area Selection) |
| `Alt` + `PrintScreen` / `Ctrl` + `Shift` + `3` | Window Screenshot |
| `Ctrl` + `PrintScreen` / `Ctrl` + `Shift` + `2` | Full Screen Screenshot |

---

## 📁 Repository Structure

```text
~/.config/niri/
├── config.kdl          # Main entrypoint
└── cfg/
    ├── animation.kdl   # Clean 200ms easing transitions
    ├── autostart.kdl   # D-Bus, GNOME Keyring, Polkit, Noctalia
    ├── display.kdl     # LG UltraGear 180Hz (Primary) + Notebook (Secondary)
    ├── input.kdl       # US-Intl & BR-ABNT2 layouts + Flat mouse profile
    ├── keybinds.kdl    # Complete keybindings & shortcuts
    ├── layout.kdl      # 8px gaps, 14px corner radius, #00BFFF -> #9D00FF border
    ├── misc.kdl        # Environment variables & browser defaults
    └── rules.kdl       # Static Workspaces 1-9 & Spotify workspace 9 rule
```

---

## 🚀 Installation & Setup

```bash
# Clone repository
git clone https://github.com/filipenevesz/niri-config.git ~/.config/niri

# Validate configuration
niri validate

# Reload Niri live
niri msg action reload-config
```

---

*Configured with ❤️ for CachyOS & Niri Wayland Compositor.*
