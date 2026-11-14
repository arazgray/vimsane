# VIMSANE
Sane VIM configuration for my personal use.

<img src="./vimsane-screenshot.jpg" alt="VIMSANE">

## Install vim-plug for Vim

These instructions are for **Vim**, not Neovim. Install Vim, Git, and curl first.

```sh
curl -fLo "$HOME/.vim/autoload/plug.vim" --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

## Download the configuration

Back up any existing configuration, then download this repository's `vimrc`:

```sh
if [ -e "$HOME/.vimrc" ]; then
    cp -p "$HOME/.vimrc" "$HOME/.vimrc.backup.$(date +%Y%m%d%H%M%S)"
fi
curl -fLo "$HOME/.vimrc" \
    https://raw.githubusercontent.com/arazgray/vimsane/main/vimrc
```

## Install the plugins

Open Vim:

```sh
vim
```

On the first launch, Vim may report `E185: Cannot find color scheme 'tokyonight'`
because the theme is not installed yet. Press Enter to continue, then run this
command **inside Vim**, not in your shell:

```vim
:PlugInstall
```

Wait for installation to finish, then close and reopen Vim.

To update installed plugins later, run `:PlugUpdate` inside Vim.

### Troubleshooting

If Vim reports `E117: Unknown function: plug#begin` or
`E492: Not an editor command: Plug`, check that vim-plug was installed at
`~/.vim/autoload/plug.vim`. The Neovim path
`~/.local/share/nvim/site/autoload/plug.vim` is not loaded by Vim.

## Keymap
`:` Commands <br>
`i` Insert <br>
`y` Copy (yank!), `yy` Copy whole line<br>
`d` Cut, `dd` Cut whole line<br>
`p` Paste<br>
`u` Undo<br>
`$` Go to End of line, `A` go to end of line and insert
`G` Go to end of doc, `gg` Move to begining<br>
`ESC` and `v` Select, `V` for line selection <br>
`qa` Close all and exit<br>
`ESC`+NUM Switch Tabs<br>
`Ctrl+t` Open tree<br>
`Ctrl+ww` Switch to Editor from Tree<br>
`Ctrl+p` Quick Open<br>
`/KEYWORD` Search<br>
`%s/KEYWORD/REPLACE-WITH/gc` Search and Replace (all, confirm before)<br>
