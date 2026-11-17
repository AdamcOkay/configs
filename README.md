# configs

Terminal setup for macOS: Ghostty, Starship, herdr. Tokyo Night, Fira Code Nerd Font.

## Install

```sh
brew install --cask ghostty font-fira-code-nerd-font
brew install starship herdr eza bat fzf zsh-autosuggestions zsh-syntax-highlighting
git clone git@github.com:YOUR_USERNAME/configs.git ~/.config
```

Add to `~/.zshrc`:

```sh
source <(fzf --zsh)
source $(brew --prefix)/share/zsh-autosuggestions/zsh-autosuggestions.zsh
source $(brew --prefix)/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
ZSH_AUTOSUGGEST_HIGHLIGHT_STYLE="fg=#565f89"
alias ls="eza --icons --group-directories-first"
alias ll="eza -l --icons --git --group-directories-first"
alias cat="bat --style=plain"
eval "$(starship init zsh)"
```

Restart the terminal.
