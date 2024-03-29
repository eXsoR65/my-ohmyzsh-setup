
# My OhMyZsh Setup

![](ohmyzsh-setup.PNG)


## Install Oh My Zsh with curl

`sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`

Note: You need to have ZSH installed before installing Oh My Zsh. Have a look at [Installing ZSH](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)


## Using a customized theme

### PowerLevel10k - my current favorite theme to use. 

[https://github.com/romkatv/powerlevel10k](https://github.com/romkatv/powerlevel10k)

*note: that you need to install fonts for it to work correctly. You can find more instructions on the powerlevel10k GitHub*

Microsoft Terminal: Open Settings [Ctrl]+[,] search for fontFace and set value to MesloLGS NF for your Linux profile (example Ubuntu).

You can find the fonts here: [Powerlevel 10k MesloLGS Nerd Font](https://github.com/romkatv/powerlevel10k#meslo-nerd-font-patched-for-powerlevel10k)
 

### Clone and set the powerlevel10k theme

`git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k`

Set `ZSH_THEME="powerlevel10k/powerlevel10k"` in your `~/.zshrc.`

## **Plugins** I use the most (zsh-autosuggestions & zsh-syntax-highlighting)
 - Download zsh-autosuggestions by
 
 `git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions`
 
 - Download zsh-syntax-highlighting by
 
 `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting`

 - Modify you .zshrc file to add the plugins Example: `nano ~/.zshrc`
 
 - Add `zsh-autosuggestions & zsh-syntax-highlighting` to  plugins()
 
 Prefered format:
 ``` text
 plugins=(
  git
  zsh-autosuggestions
  zsh-syntax-highlighting
)
 ```
 
### Shell Parameter Highlighting (requires zsh-syntax-highlighting plugin) 
Special Thanks to user **titus#6602** from the Oh-My-Zsh discord for sharing this awesome customization.

```bash
export ZSH_HIGHLIGHT_HIGHLIGHTERS=(main brackets regexp)
typeset -A ZSH_HIGHLIGHT_REGEXP
ZSH_HIGHLIGHT_REGEXP+=(' -{1,2}[a-zA-Z0-9_-]*' fg=008)
```
Example: It will highlight the parameters like -- or - in grey lke you see below. 
![](parameter-highlighting.png)


### Reload your .zshrc to apply changes with `exec zsh`.
###### Note you shouldn't not be using `source ~/.zshrc` when using ohmyzsh, just takes longer and forces to reload everything when its not needed. 


## If you want other users to have ohmyzsh then just do the below.
**Make sure that zsh is already installed.**
Then login as another user of the system:

- `export ZSH=/home/username_here/.oh-my-zsh`
- `sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`

 ## Ref
 - [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)
 - [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
 - [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
