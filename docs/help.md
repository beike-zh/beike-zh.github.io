## 配置文件

> `WSL2-Ubuntu` 

### basic
```bash
sudo apt update
sudo apt upgrade
sudo apt install zsh python3-pip lua5.1 luajit curl libffi-dev libffi7 libgmp-dev libgmp10 libncurses-dev libncurses5 libtinfo5
chsh -s /usr/bin/zsh
zsh 
# 选0 
```
添加 `source ~/dotfiles/init/zsh/init.zsh` 到 `.zshrc`

### ppa
```bash
sudo add-apt-repository ppa:neovim-ppa/unstable
sudo add-apt-repository ppa:git-core/ppa
sudo apt update
```

### `zsh`
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/zdharma/zinit/master/doc/install.sh)"
# 安装 zinit
# 选 n, 然后我手动配置
```

### git
```bash
git config --global init.defaultBranch main
```

### neovim
```bash 
mk .config && cd .config
mk nvim && cd nvim
vim init.vim
```
在 `~/.config/nvim/init.vim` 中添加 `source ~/dotfiles/init/nvim/init.vim`

检查
`:echo has("python3")`
如果返回 `1`, 不用处理, 否则
`pip3 install --user pynvim`

### 网络问题

此方案针对于使用 `WSL2` 的用户
```bash
sudo vim /etc/wsl.conf #设置如下
# 然后关闭 WSL2 
#在windows中使用
wsl --shutdown
# 然后重开WSL
sudo rm /etc/resolv.conf
sudo vim /etc/resolv.conf
# 添加如下内容
```

>wsl.conf
```ini
[network]
generateResolvConf = false
```
> resolv.conf
```ini
nameserver 8.8.8.8
# 或者其他, 我这里 8.8.8.8 效果比较好
# nameserver1.1.1.1
```