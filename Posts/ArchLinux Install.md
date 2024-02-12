# Headers
1. [[#Install Paru (aur helper)]]
2. [[#Install System apps]]
3. [[#Install user apps]]
4. [[#Tools]]
	1) [[#TLP and tlp gui (need chaotic aur or yay)]] 
	2) [[#ZSH]]
	3) [[#Fonts]]


## Install Paru (aur helper):
```bash
git clone https://aur.archlinux.org/paru-bin/
cd paru-bin
makepkg -sric
```
## Install System apps:
```bash
paru -S zsh bat btop system76-power neovim starship mpv yt-dlp github-cli --noconfirm
```

## Install user apps:
```bash
paru -S vlc telegram-desktop obsidian firefox qbittorrent --noconfirm
```

# Tools
## TLP and tlp gui (need chaotic aur or yay)
```bash
paru -S tlp tlpui
systemctl enable --now tlp
```

## ZSH
```bash
# Zsh
chsh
/usr/bin/zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-history-substring-search ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-history-substring-search
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

# add to plugins in .zshrc
zsh-autosuggestions zsh-history-substring-search zsh-syntax-highlighting

starship preset pastel-powerline -o ~/.config/starship.toml
```

## Fonts
```bash
paru -S ttf-jetbrains-mono-nerd ttf-firacode-nerd
```