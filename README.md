# nvim-config

Personal Neovim configuration, usable independently of chezmoi.

## Install

With Neovim and Git installed, clone the configuration on Linux:

```sh
git clone https://github.com/cotrin8672/nvim-config.git ~/.config/nvim
```

On Windows, Neovim normally reads `%LOCALAPPDATA%\nvim`. The
[dotfiles repository](https://github.com/cotrin8672/dotfiles) manages this
repository at `~/ghq/github.com/cotrin8672/nvim-config` through a chezmoi
`git-repo` external and links the Neovim configuration directory to it.

Start Neovim to let lazy.nvim install the configured plugins. Language tools
and other external programs must be installed separately.

## Update

Run `git pull --ff-only` in the configuration directory, or run
`chezmoi update` when using the dotfiles repository.

## Tests

Run the tests from this repository's root. They use the locally installed
Neovim plugins; the command for each test is recorded at the top of its file.

```sh
nvim --headless -u NONE -i NONE -n -l tests/nvim_tabby.lua
```

`docs/` contains the existing Neovim cheat sheet and investigation notes.
