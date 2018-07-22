# Stripy Sock Dotfiles

## Requirements

Set zsh as your login shell:

```sh
chsh -s $(which zsh)
```

## Install

Install [rcm](https://github.com/thoughtbot/rcm):

```sh
brew tap thoughtbot/formulae
brew install rcm
```

Check out the dotfiles:

```sh
git clone https://github.com/stripysock/dotfiles.git ~/.dotfiles-stripysock
```

Install the dotfiles:

```sh
env RCRC=~/.dotfiles-icelab/rcrc rcup
```

## Make your own customizations

Put your customizations in dotfiles appended with `.local`:

* `~/.aliases.local`
* `~/.gitconfig.local`
* `~/.zshrc.local`

For example, your `~/.aliases.local` might look like this:

```
# Personal git shortcuts
alias gs='git status'
alias gd='git diff'
```

Your `~/.gitconfig.local` might look like this:

```
[user]
  name = Your Name
  email = you@stripysock.com.au
```

Your `~/.zshenv.local` might look like this:

```
# Use Sublime Text as default editor
export VISUAL=subl
export EDITOR=$VISUAL
```

## Combine with your personal dotfiles

The `rcrc` configuration in these dotfiles looks for a separate `~/.dotfiles-personal` direcotry. If you create this directory, fill it with dotfiles, and then run `rcup`, those personal dotfiles will be used in combination with (and in preference to) these ones. See [Philip's dotfiles](https://github.com/blackp/dotfiles) as an example.

## Credits

Thanks to Thoughtbot for [their dotfiles](https://github.com/thoughtbot/dotfiles), and [rcm](https://github.com/thoughtbot/rcm).

Thanks to Tim Riley and Icelab for [their dotfiles](https://github.com/icelab/dotfiles), which formed the basis for this collection.

These dotfiles are maintained by [Stripy Sock](http://stripysock.com.au/).
