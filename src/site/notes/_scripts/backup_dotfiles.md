---
{"dg-publish":true,"permalink":"/scripts/backup-dotfiles/","title":"Backup linux dotfiles","tags":["configuration","linux","utility"]}
---


# Backup linux dotfiles

Script is generated by ChatGPT and it should automate backup of linux configuration files by utilising git bare repository. Before running you should review the script by yourself. Never trust the output of AI and large language models without verification by trusted human with real life experience.

```bash
#!/bin/bash

# Generated by Large Language Model, ChatGPT
# Review the script and run in safe environment first

# Set variables
DOTFILES_REPO="$HOME/.dotfiles"
GIT_REMOTE="git@github.com:MorphZG/dotfiles.git"

# Create bare repository if not exists
if [ ! -d "$DOTFILES_REPO" ]; then
    git init --bare $DOTFILES_REPO
    echo "Initialized bare git repository at $DOTFILES_REPO"
fi

# Setup alias in shell configuration
ALIAS_CMD="alias config='/usr/bin/git --git-dir=$DOTFILES_REPO --work-tree=$HOME'"
if ! grep -Fxq "$ALIAS_CMD" ~/.bashrc; then
    echo "$ALIAS_CMD" >> ~/.bashrc
    echo "Added 'config' alias to .bashrc"
fi
source ~/.bashrc

# Configure git to ignore untracked files
config config --local status.showUntrackedFiles no

# Commit initial dotfiles (customize this list)
DOTFILES=(
    .bashrc
    .zshrc
    .vimrc
    .gitconfig
    .config/nvim/init.vim
)

for file in "${DOTFILES[@]}"; do
    if [ -f "$HOME/$file" ] || [ -d "$HOME/$file" ]; then
        config add "$file"
        echo "Added $file to dotfiles repo"
    fi
done

config commit -m "Initial commit of dotfiles"

# Set remote and push
config remote add origin $GIT_REMOTE
config push -u origin master

echo "Dotfiles backed up to $GIT_REMOTE"
```

## Reference

- [[00_Fleeting_inbox/git bare repository\|git bare repository]] - personal note
- [[01_Reference/software tools/stow the dotfiles\|stow the dotfiles]] - personal note
