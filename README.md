# My ZSH setting
My Simple ZSH setting for my terminal

## Recipe

### Install [zsh](https://aur.archlinux.org/):
```zsh
sudo pacman -Sy zsh
```

### Install [Oh My Zsh](https://ohmyz.sh/)
```zsh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### Install [Powerlevel10k](https://github.com/romkatv/powerlevel10k) in [Oh My Zsh](https://ohmyz.sh/) custom directory
```zsh
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

### Install [Nerfonts](https://www.nerdfonts.com/font-downloads)
Recommend Download: [Fira Nerd Fonts](https://github.com/ryanoasis/nerd-fonts/releases/download/v2.2.2/FiraCode.zip), extract downloaded fonts and install using any Font Management `1` to System `2`.

**Linux:** Font Management

![Screenshot_20221201_002615](https://user-images.githubusercontent.com/72515939/204853958-d250a796-f635-463a-b932-8ddcac969c37.png)

**macOS:** Font Book

![FontsBook](https://user-images.githubusercontent.com/72515939/204847668-89a8fd2c-a492-4d09-8442-f1a2d9870eef.png)

### Install zsh-autosuggestions
```zsh
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

### Install highlight syntax
```zsh
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

### Configure powerlevel10k
```zsh
p10k configure 
```

## Beautify

### Setting Terminal
Use downloaded font on terminal settings

> **Note**: For better result on macOS, install iTerm2 and set font using downloaded font.
```zsh
brew install iterm2
```

![iTerm2](https://user-images.githubusercontent.com/72515939/204852071-859426ba-fda4-4c65-9fd2-64ea7b3baeb9.png)

### Editing zsh config
```zsh
sudo nano ~/.zshrc
```

Set this section

```nano
# Set name of the theme to load --- if set to "random", it will
# load a random theme each time oh-my-zsh is loaded, in which case,
# to know which specific one was loaded, run: echo $RANDOM_THEME
# See https://github.com/ohmyzsh/ohmyzsh/wiki/Themes
ZSH_THEME="powerlevel10k/powerlevel10k"
```

and add `zsh-autosuggestions` + `zsh-syntax-highlighting`

```nano
# Which plugins would you like to load?
# Standard plugins can be found in $ZSH/plugins/
# Custom plugins may be added to $ZSH_CUSTOM/plugins/
# Example format: plugins=(rails git textmate ruby lighthouse)
# Add wisely, as too many plugins slow down shell startup.
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
```

* Linux

![Screenshot_20221201_002954](https://user-images.githubusercontent.com/72515939/204854357-938acc20-42c6-46ac-8e8c-13b750ec5eab.png)

* macOS

![iTerm](https://user-images.githubusercontent.com/72515939/204852190-6e7d3746-3856-4b01-8bd6-26a9e79e3933.png)
