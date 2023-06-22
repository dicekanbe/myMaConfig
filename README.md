# My workspace on macOS


## install

```bash
ssh-keygen -t ed25519
```

Run install script
```bash
curl -fsSL https://raw.githubusercontent.com/dicekanbe/workspace/HEAD/install.sh | WORKSPACE_REPOSITORY_URL=git@github.com:dicekanbe/workspace.git && zsh -
```


# Install ansible
brew install ansible
```
## Provisioning

```bash
cd ~/provision
ansible-playbook playbook.yml -i hosts
```

## Terminal font setting

- Family: FiraCode Nerd Font
- Typeface: Regular
- Size: 12
- Character Spacing: 1
- Line Spacing: 0.85
