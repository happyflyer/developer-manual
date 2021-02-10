# Oh My Zsh 使用

## 1. zsh

```bash
sudo apt-get install zsh
```

## 2. oh my zsh

```bash
# sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
sh -c "$(curl -fsSL https://gitee.com/mirrors/oh-my-zsh/raw/master/tools/install.sh)"
```

## 3. 插件

```bash
sudo apt-get install -y autojump git
```

```bash
git clone https://gitee.com/mirror-github/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
```

```bash
git clone https://gitee.com/mirror-github/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
```

## 4. 配置

```bash
vim ~/.zshrc
```

```properties
plugins=(
    git
    zsh-autosuggestions
)
```

```properties
. /usr/share/autojump/autojump.sh
source $ZSH_CUSTOM/plugins/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
source $ZSH_CUSTOM/plugins/zsh-autosuggestions/zsh-autosuggestions.zsh
```
