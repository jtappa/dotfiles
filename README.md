# dotfiles

personal setup for a new computer with dev environment

## oh-my-zsh

Make an alias to the theme file in this repo

Also install:
* `zsh-autosuggestions`
* `zsh-syntax-highlighting`

Then add to `.zshrc`:

```bash
if [ -e /usr/local/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh ]; then
    source /usr/local/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
fi

if [ -e /usr/local/share/zsh-autosuggestions/zsh-autosuggestions.zsh ]; then
    source /usr/local/share/zsh-autosuggestions/zsh-autosuggestions.zsh
    bindkey '^ ' autosuggest-accept
fi
```

## Useful VS Code extensions

* Code Spell Checker
* Markdown Table Formatter
* Rainbow CSV
* Excel Viewer
* Sort Lines by Selection

## Setup auto signing in git

To configure your Git client to sign commits by default for a local repository, in Git versions 2.0.0 and above, run `git config commit.gpgsign true`. To sign all commits by default in any local repository on your computer, run `git config --global commit.gpgsign true`.

To store your GPG key passphrase so you don't have to enter it every time you sign a commit, we recommend using the following tools:

For Mac users, the GPG Suite allows you to store your GPG key passphrase in the Mac OS Keychain.
For Windows users, the Gpg4win integrates with other Windows tools.
You can also manually configure gpg-agent to save your GPG key passphrase, but this doesn't integrate with Mac OS Keychain like ssh-agent and requires more setup.
