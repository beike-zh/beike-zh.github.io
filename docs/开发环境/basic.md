# 开发环境配置

> `WSL2-Ubuntu` 

## 基本配置
```bash
sudo sed -i 's/archive.ubuntu.com/mirrors.ustc.edu.cn/g' /etc/apt/sources.list
sudo apt update
sudo apt upgrade
sudo apt install zsh python3-pip lua5.3 build-essential curl libffi-dev libffi7 libgmp-dev libgmp10 libncurses-dev libncurses5 libtinfo5
chsh -s /usr/bin/zsh
zsh 
# 选2 
```

## PPA相关
```bash
sudo add-apt-repository ppa:kelleyk/emacs
sudo apt update
sudo apt install emacs27-nox
```

## Shell
```bash
curl -sL --proto-redir -all,https https://raw.githubusercontent.com/zplug/installer/master/installer.zsh | zsh
# 安装 zplug
zplug install
```

添加 `source ~/dotfiles/init/zsh/init.zsh` 到 `.zshrc`

## Neovim

在 `~/config/nvim/init.vim` 中添加 `source ~/dotfiles/init/nvim/init.vim` 

## Haskell

> 使用 `ghcup`

```bash
curl --proto '=https' --tlsv1.2 -sSf https://get-ghcup.haskell.org | sh

ghcup install 8.10.2
ghcup set ghc 8.10.2
```

> Cabal.config