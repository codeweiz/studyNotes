## mba m1安装Homebrew

```shell
/bin/zsh -c "$(curl -fsSL https://gitee.com/huwei1024/HomebrewCN/raw/master/Homebrew.sh)"
```

```shell
touch ~/.zshrc
open -e ~/.zshrc
```

```shell
# 加入环境变量
export PATH=/opt/homebrew/bin:$PATH
export PATH=/opt/homebrew/sbin:$PATH
```

```shell
# 环境生效
source ~/.zshrc
```



## mba m1安装NVM

- 保证环境中没有node

  ```shell
  sudo npm uninstall npm -g
  sudo rm -rf /usr/local/lib/node /usr/local/lib/node_modules /var/db/receipts/org.nodejs.*
  sudo rm -rf /usr/local/include/node /Users/$USER/.npm
  sudo rm /usr/local/bin/node
  sudo rm /usr/local/share/man/man1/node.1
  sudo rm /usr/local/lib/dtrace/node.d
  ```

  

- brew安装nvm

  ```shell
  arch -x86_64 zsh
  arch -arm64 brew install nvm
  ```

  

- 在~/.zshrc文件中加入

  ```shell
  export NVM_DIR="$HOME/.nvm"
    [ -s "/opt/homebrew/opt/nvm/nvm.sh" ] && . "/opt/homebrew/opt/nvm/nvm.sh"  # This loads nvm
    [ -s "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm" ] && . "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm"  # This loads nvm bash_completion
  ```

  ```shell
  source ~/.zshrc
  ```

  

- 查看NVM

  ```shell
  nvm -v
  ```



## mba m1安装node

- 有了Rosetta 2转译的nvm，安装node就方便了

  ```shell
  nvm install [版本号]
  nvm install node
  nvm install 10.15
  ```

- 切换node环境

  ```shell
  nvm use [版本号]
  nvm use 10.15
  ```

  

- 查看nvm当前node

  ```shell
  nvm current
  ```

  

- NVM常用命令

  ```shell
  # 帮助信息
  nvm --help
  
  # 查看NVM版本
  nvm --version
  
  # 安装指定版本的Node
  nvm install [-s] [verison]
  
  # 重新安装特定版本的Node
  nvm install -reinstall-packages-from=[version]
  
  # 安葬最新的LTS版本Node
  nvm install --lts=[LTS name]
  
  # 跳过默认包安装
  nvm install --skip-default-packages
  
  #更新npm
  nvm install --lastest-npm
  
  # 静默安装Node
  nvm install --no-progress
  
  # 卸载特定版本
  nvm uninstall [version]
  ```

  软连接作用

  ```text
  > ln -s ~/.nvm/versions/node/<latest-node-lts-version>/ /usr/local/Cellar/node
  ```

  nvm 卸载 node

  ```text
  > nvm uninstall v10.16.2
  Uninstalled node v10.16.2
  ```