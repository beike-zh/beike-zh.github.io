## 此博客开发环境设置

### 默认使用 `main` 分支

#### 确保 git > 2.28, 方可使用下列命令

```bash
sudo add-apt-repository ppa:git-core/ppa
sudo apt update 
sudo apt upgrade

git config --global init.defaultBranch main

```

#### Material for MkDocs

```bash

pip install mkdocs-material
mk blog && cd blog
mkdocs new .

git init


```