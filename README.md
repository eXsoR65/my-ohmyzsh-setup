# My OhMyZsh customizationing

## Install with curl
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

## Using my Customized Theme that inclused hostname in the path. 
I custumized robbyrussell.zsh-theme to add hostname in the prompt. The orginal can by found here: https://github.com/ohmyzsh/ohmyzsh/blob/master/themes/robbyrussell.zsh-theme

Download mytheme by
```
 curl -o $ZSH_CUSTOM/themes/mytheme.zsh-theme-test https://raw.githubusercontent.com/eXsoR65/my-ohmyzsh-customizationing/main/mytheme.zsh-theme
```

- Modify ZSH_THEME="robbyrussell" to ZSH_THEME="mytheme"

## Enabling Plugins (zsh-autosuggestions & zsh-syntax-highlighting)
 - Download zsh-autosuggestions by
 
 `git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions`
 
 - Download zsh-syntax-highlighting by
 
 `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting`

 - `nano ~/.zshrc` find `plugins=(git)`
 
 - Append `zsh-autosuggestions & zsh-syntax-highlighting` to  `plugins()` like this 
 
 `plugins=(git zsh-autosuggestions zsh-syntax-highlighting)`
 
 - Reopen terminal