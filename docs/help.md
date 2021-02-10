## 哈啊

> `WSL2-Ubuntu` 

### basic
```bash
sudo apt update
sudo apt upgrade
sudo apt install zsh python3-pip lua5.3 build-essential curl libffi-dev libffi7 libgmp-dev libgmp10 libncurses-dev libncurses5 libtinfo5
chsh -s /usr/bin/zsh
zsh 
# 选2 
```

### ppa
```bash
sudo add-apt-repository ppa:neovim-ppa/unstable
sudo add-apt-repository ppa:git-core/ppa
sudo apt update
```

### `zsh`
```bash
curl -sL --proto-redir -all,https https://raw.githubusercontent.com/zplug/installer/master/installer.zsh | zsh
# 安装 zplug
zplug install
```

添加 `source ~/dotfiles/init/zsh/init.zsh` 到 `.zshrc`

### git
```bash
git config --global init.defaultBranch main
```

### neovim

在 `~/config/nvim/init.vim` 中添加 `source ~/dotfiles/init/nvim/init.vim` 

### haskell

> 使用 `ghcup`

我用不来 `stack`

```bash
curl --proto '=https' --tlsv1.2 -sSf https://get-ghcup.haskell.org | sh

ghcup install 9.0.x
ghcup set ghc 9.0.x
```
