# my-ohmyzsh-customizationing
My OhMyZsh customizationing


Install with curl

sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"


Enabling Plugins (zsh-autosuggestions & zsh-syntax-highlighting)

Download zsh-autosuggestions by

git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions

Download zsh-syntax-highlighting by

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting


nano ~/.zshrc find plugins=(git)

Append zsh-autosuggestions & zsh-syntax-highlighting to plugins() like this

plugins=(git zsh-autosuggestions zsh-syntax-highlighting)

Reopen terminal
