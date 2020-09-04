# To change shell
`chsh -s $(which zsh)`

# To keyboard layout

## To know current keyboard layout
`localectl status`

## To list available keyboard layout
`localectl list-keymaps | rg dvor`

## To set keyboard layout
`localectl set-keymap us-dvorak-alt-intl`

`localectl set-x11-keymap dvorak`
