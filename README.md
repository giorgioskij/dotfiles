# dotfiles
Years of OCD carefully assembled in a juicy directory of invisible files

--- 
## Setting up your fresh OSX

### _Basic tools_


#### install command line developer tools
```
xcode-select --install
```

#### install homebrew
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

#### install the GitHub command line tool
```
brew install gh

gh auth login
```

<br/>
<br/>

### _Clone dotfiles repo_


#### create dev directory, and clone dotfiles
```
cd
mkdir dev
cd dev
gh repo clone giorgioskij/dotfiles
cd
```
<br/>
<br/>

### _Terminal configuration_



#### install oh-my-zsh
```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
#### install and set powerlevel10k theme
```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

sed -i '' 's/ZSH_THEME="robbyrussell"/ZSH_THEME="powerlevel10k\/powerlevel10k"/g' .zshrc
```
#### choose and import a theme from .terminal/  


<br/>
<br/>

### _Vim configuration_

```
mkdir -p ~/.vim/colors
ln -fs ~/dev/dotfiles/vim/.vimrc
ln -s ~/dev/dotfiles/vim/.nord.vim ~/.vim/colors/
source ~/.vimrc
```

<br/>
<br/>

### _Install basic apps_


```
brew install visual-studio-code atom firefox spotify teamviewer karabiner-elements
```

<br/>
<br/>

### _Setup karabiner_

Open the app karabiner-elements and follow the procedure to allow the required privileges

#### link the configuration file
```
ln -fs ~/dev/dotfiles/.karabiner/karabiner.json ~/.config/karabiner
```



