# 🚀 Starship Prompt Configuration

This repository contains my custom **Starship** prompt configuration.

---

## 📦 Requirements

Before using this config, make sure you have:

- ✅ Starship installed → https://starship.rs/
- ✅ A **Nerd Font** installed (icons will NOT render correctly without it)

### 🔤 Recommended Font

I highly recommend:

👉 **FiraMono Nerd Font**

Download it here:

- Official Nerd Fonts download page:  
  https://www.nerdfonts.com/font-downloads

- Direct GitHub releases page:  
  https://github.com/ryanoasis/nerd-fonts/releases

After downloading:

1. Install the font  
2. Set it as your terminal font  
3. Restart your terminal  

---

## ⚙️ Installation

Copy this configuration into:

```bash
~/.config/starship.toml
```

Or on Windows:

```bash
C:\Users\<your-username>\.config\starship.toml
```

---

## 🛠 Configuration

```toml
"$schema" = 'https://starship.rs/config-schema.json'

format = """
$username\
$hostname\
$directory\
$git_branch\
$git_state\
$git_status\
$cmd_duration\
$line_break\
$python\
$character"""

[directory]
style = "#fefcf9"

[character]
success_symbol = "[❯](#5de2e9)"
error_symbol = "[❯](#EB6959)"
vimcmd_symbol = "[❮](#8aefaf)"

[git_branch]
format = "[$branch]($style)"
style = "#e28b28"

[git_status]
format = "[[( $conflicted$untracked$modified$staged$renamed$deleted)]($style) ($ahead_behind$stashed)]($style)"
style = "#8aefaf"

conflicted = "[⚔️${count}](bold #F0EC35) "
untracked = "[?${count}](cyan) "
modified = "[~${count}](#F0EC35) "
staged = "[+${count}](#35F058) "
renamed = "[»${count}](blue) "
deleted = "[-${count}](#F0EC35) "

ahead = "[↑${count}](#35F058) "
behind = "[↓${count}](#F0EC35) "
diverged = "[⇕↑${ahead_count}↓${behind_count}](#F0EC35 bold) "
stashed = "[≡${count}](#35F058) "

[git_state]
format = '\([$state( $progress_current/$progress_total)]($style)\) '
style = "#e28b28"

[cmd_duration]
format = "[$duration]($style) "
style = "#F0EC35"

[python]
format = "[$virtualenv]($style) "
style = "#e28b28"
detect_extensions = []
detect_files = []
```
