# Manjaro update error fixes
## Solve error: cannot find the fakeroot binary
`sudo pacman -S base-devel`

## To select fastest mirror from 5 
`sudo pacman-mirrors --fasttrack 5 && sudo pacman -Syyu`

## Update failure
`sudo pacman -Scc`
`sudo mv /etc/pacman.d/gnupg /etc/pacman.d/gnupg.old`

## To refresh update keys
`sudo pacman-key --init` 
`sudo pacman-key --populate`
`sudo pacman-key --refresh-keys`
`sudo pacman -Sy archlinux-keyring`

## To remove cached packages
`sudo pacman  -R $(pacman -Qtdq)`

## Troubleshooting update errors
`sudo rm /etc/resolv.conf`
`sudo sh -c 'echo "nameserver 8.8.8.8" > /etc/resolv.conf`
