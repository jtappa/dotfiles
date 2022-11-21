# dotfiles

personal setup for a new computer with dev environment

## oh-my-zsh

Make a symbolic link to the theme file in this repo

```bash
ln -s /Users/USERDIR/git-repos/dotfiles/jorie.zsh-theme /Users/USERDIR/.oh-my-zsh/themes/jorie.zsh-theme
```

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

* GitLens
* Code Spell Checker
* Markdown Table Formatter
* Rainbow CSV
* Excel Viewer
* Sort Lines by Selection

## Setup auto signing in git

[Follow instructions](https://docs.github.com/en/github/authenticating-to-github/about-commit-signature-verification) to set up a gpg signing key, add it to git, and add it to your .zshrc.

To sign all commits by default in any local repository on your computer, run `git config --global commit.gpgsign true`.

To store your GPG key passphrase so you don't have to enter it every time you sign a commit, we recommend using the following tools:

For Mac users, the GPG Suite allows you to store your GPG key passphrase in the Mac OS Keychain.
For Windows users, the Gpg4win integrates with other Windows tools.
You can also manually configure gpg-agent to save your GPG key passphrase, but this doesn't integrate with Mac OS Keychain like ssh-agent and requires more setup.
