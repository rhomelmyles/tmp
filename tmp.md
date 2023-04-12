# Installation guide

## Hosts

```
# Host addresses
127.0.0.1  localhost
127.0.1.1  alex
::1        localhost ip6-localhost ip6-loopback
ff02::1    ip6-allnodes
ff02::2    ip6-allrouters

192.168.100.5 alex
```

## Base installations

* curl, wget, git
* zsh
* rofi
* flameshot
* nodejs
* rust
* fzf
* nnn
* xclip
* volumeicon
* ripgrep
* fd
* bat
* greenclip: https://github.com/erebe/greenclip and create symbolic link to /usr/bin/greenclip

## Meslo fonts

```sh
wget https://github.com/ryanoasis/nerd-fonts/releases/download/v2.3.3/Meslo.zip 
mkdir -p ~/.local/share/fonts
unzip Meslo.zip -d ~/.local/share/fonts
rm ~/.local/share/fonts/*Windows*
rm Meslo.zip
fc-cache -fv
```

## fzf

```
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
```

## Oh my zsh

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## Powerlevel10k theme

```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

## Oh my zsh plugins

```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

## Replace ZSH config

```
mv ~/.zshrc ~/.zshrc.BAK
cp ~/fedora-files/zshrc ~/.zshrc
```

## Install nnn

