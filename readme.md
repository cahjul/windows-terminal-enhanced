# Windows Terminal + Oh My Posh Setup Guide

A beautiful and complete setup to enhance your Windows Terminal, PowerShell, Git Bash, CMD, and WSL experience.

---

## ✅ 1. Install Windows Terminal

Download from **Microsoft Store**.

---

## ✅ 2. Set Windows Terminal as Default

Go to:
**Settings → System → For Developers → Terminal**
Select **Windows Terminal**.

---

## ✅ 3. Install Nerd Font

Download from:
[https://github.com/ryanoasis/nerd-fonts/releases](https://github.com/ryanoasis/nerd-fonts/releases)

After installation:

* Open **Windows Terminal Settings**
* Go to **Defaults → Appearance → Font**
* Choose your Nerd Font
* or you can use this oh-my-posh font install command as long oh-my-posh installed.

---

## ✅ 4. Install Windows Terminal Theme

Visit:
[https://windowsterminalthemes.dev/](https://windowsterminalthemes.dev/)

To apply:

1. Open Windows Terminal
2. Go to **Settings → Open JSON File**
3. Paste the theme configuration

---

## ✅ 5. Install Oh-My-Posh

Official guide:
[https://ohmyposh.dev/docs/installation/windows](https://ohmyposh.dev/docs/installation/windows)

---

## ✅ 6. Configure Shell Prompt

Follow the setup guide:
[https://ohmyposh.dev/docs/installation/prompt](https://ohmyposh.dev/docs/installation/prompt)

---

## ✅ 7. Configure Oh My Posh for Git Bash

```
test -f ~/.profile && . ~/.profile
test -f ~/.bashrc && . ~/.bashrc
nano ~/.bashrc
```

Inside `.bashrc`:

```
eval "$(oh-my-posh init bash --config https://raw.githubusercontent.com/JanDeDobbeleer/oh-my-posh/refs/heads/main/themes/atomic.omp.json)"
```

---

## ✅ 8. Configure for PowerShell

Edit profile:
**Microsoft.PowerShell_profile.ps1**

Add:

```
oh-my-posh init pwsh --config 'https://raw.githubusercontent.com/JanDeDobbeleer/oh-my-posh/refs/heads/main/themes/atomic.omp.json' | Invoke-Expression
```

---

## ✅ 9. Configure for CMD

Install **clink**, then run:

```
clink set ohmyposh.theme https://raw.githubusercontent.com/JanDeDobbeleer/oh-my-posh/refs/heads/main/themes/atomic.omp.json
```

---

## ✅ 10. Configure for WSL (Ubuntu/Debian)

Install Oh My Posh using:

```
curl -s https://ohmyposh.dev/install.sh | bash -s
```

*(Ensure you have `curl` and `unzip` installed.)*

---

## 🧩 11. Ensure Oh My Posh Loads Automatically (WSL)

Edit `.bashrc`:

```
nano ~/.bashrc
```

Add the following:

```
# ensure always load posh
export PATH=$PATH:~/.local/bin
if [ -f $(which oh-my-posh) ]; then
  eval "$(oh-my-posh init bash)"
fi

# load posh theme
if [ -f $(which oh-my-posh) ]; then
  eval "$(oh-my-posh init bash --config https://raw.githubusercontent.com/JanDeDobbeleer/oh-my-posh/refs/heads/main/themes/atomic.omp.json)"
fi
```

---

## 🎉 Done!

Your terminal is now modern, clean, and fully themed with Nerd Fonts + Oh My Posh + custom themes.
*This readme.md is generated using OpenAI, however the step is tested on my device :P.
