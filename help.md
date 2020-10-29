## 默认使用 `main` 分支

### 确保 git > 2.28

```bash
sudo add-apt-repository ppa:git-core/ppa
sudo apt update && upgrade

git config --global init.defaultBranch main

```