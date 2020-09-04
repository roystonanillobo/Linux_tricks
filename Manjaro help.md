#Manjaro Beginner's Tour: Package Management 
#Manjaro - Beginner's Tour 
Common command line examples:

## To update system
### Ubuntu code
`sudo apt-get update && apt-get upgrade`
### Manjaro code
`sudo pacman -Syu` 

## To search packages
### Ubuntu code
`apt-cache search package-x` 
### Manjaro code
`pacman -Ss package-x`

## To install packages
### Ubuntu code
`sudo apt-get install package-x` 
### Manjaro code
`sudo pacman -S package-x` 

## To install packages from other repository
### Ubuntu code
`sudo add-apt-repository ppa://website/package-x && sudo apt-get update && sudo apt-get install package-x` 
### Manjaro code
`yay package-x`

## To update AUR packages
### Manjaro code
`yay -Su`

### Reference:
https://youtu.be/VU8EA-s3_hU?list=PL426FzyFBwBo_kwxfAwyKCKsviq54SfA0

