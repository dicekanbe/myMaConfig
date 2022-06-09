# My workspace on macOS

## Prepare for provisioning

```bash
# Create bare repository
mkdir $HOME/myMaConfig
git init --bare $HOME/myMaConfig 
ssh-keygen -t rsa
alias config='git --git-dir=$HOME/myMaConfig/ --work-tree=$HOME'
config config status.showUntrackedFiles no
config config pull.rebase true
config remote add origin git@github.com:dicekanbe/myMaConfig.git
config pull origin master
config branch --set-upstream-to=origin/master

# Install homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
eval "$(/opt/homebrew/bin/brew shellenv)"
brew update
brew upgrade

# Install ansible
brew install ansible
```
## Provisioning

```bash
cd ~/provision
ansible-playbook playbook.yml -i hosts
rake serverspec:all
```

## Terminal font setting

- Family: FiraCode Nerd Font
- Typeface: Regular
- Size: 12
- Character Spacing: 1
- Line Spacing: 0.85
