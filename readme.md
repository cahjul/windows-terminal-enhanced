1. Install Windows Terminal from Microsoft Store
2. Set Windows Terminal as default terminal instead of powershell at Setting > System > For developers.
3. Install font from here: https://github.com/ryanoasis/nerd-fonts/releases and choose your font from Windows Terminal Setting > Default > Appearence > Font.
4. Install Theme from https://windowsterminalthemes.dev/ and apply at Terminal Setting > Open JSON Files.
5. Install Oh-My-Posh by using this instruction https://ohmyposh.dev/docs/installation/windows .
6. Configure Shell using this https://ohmyposh.dev/docs/installation/prompt .
7. For Git Bash, 
test -f ~/.profile && . ~/.profile
test -f ~/.bashrc && . ~/.bashrc
nano ~/.bashrc
Inside .bashrc
eval "$(oh-my-posh init bash --config https://raw.githubusercontent.com/JanDeDobbeleer/oh-my-posh/refs/heads/main/themes/atomic.omp.json)"
9. For PowerShell, Microsoft.PowerShell_profile.ps1.
oh-my-posh init pwsh --config 'https://raw.githubusercontent.com/JanDeDobbeleer/oh-my-posh/refs/heads/main/themes/atomic.omp.json' | Invoke-Expression
10. For CMD, you need to install clink.    
clink set ohmyposh.theme https://raw.githubusercontent.com/JanDeDobbeleer/oh-my-posh/refs/heads/main/themes/atomic.omp.json
11. For WSL Ubuntu/Debian, install curl -s https://ohmyposh.dev/install.sh | bash -s (don't forget install curl and unzip)

12. # esnure always load posh
export PATH=$PATH:~/.local/bin
if [ -f $(which oh-my-posh) ]; then
  eval "$(oh-my-posh init bash)"
fi

nano .bashrc
# esnure always load posh
export PATH=$PATH:~/.local/bin
if [ -f $(which oh-my-posh) ]; then
  eval "$(oh-my-posh init bash)"
fi

# load posh theme
if [ -f $(which oh-my-posh) ]; then
  eval "$(oh-my-posh init bash --config https://raw.githubusercontent.com/JanDeDobbeleer/oh-my-posh/refs/heads/main/themes/atomic.omp.json)"
fi
