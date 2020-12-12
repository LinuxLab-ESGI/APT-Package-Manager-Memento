# APT-Package-Manager-Memento

Memento for APT to manage our package.

APT (**A**dvanced **P**ackage **T**ool) is a package manager Debian and Debian's like distros.

Debian distors uses a packaging sytem called **dpkg** (Debian package). It provides programs and applications for installation in the way that we don't have to manually build a program from the source code. There is a dpkg manager but APT is more friendly to use.

>Here we are using `apt` (new way) and not `apt-get` (old way), apt has more advantages over apt-get such as aprogress bar, prompoting the number of package that can be upgraded, simplier commands, etc.

## Update package database

`sudo apt update`

## Update installed packages

`sudo apt upgrade`

`sudo apt update && sudo apt upgrade -y`

## Install new packages

`sudo apt install <package_name>`
`sudo apt install <package_name> <package_name2>`

Install without upgrading :  
`sudo apt install <package_name> --no-upgrade`

Install only upgrading :  
`sudo apt install <package_name> --only-upgrade`

Install with specific version number :
`sudo apt install <package_name>=<version_number>`

If we downloaded a **.deb** file, we can install it with :  
`sudo dpkg -i fichier.deb`
`sudo apt install -f` (sintalling dependencies)
Or :
`sudo apt install ./fichier.deb`

## Remove packages

`sudo apt remove <package_name>`
`sudo apt purge <package_name>`

## Search for some informations

`apt search <search term>`
`apt show <package_name>`
`apt list --upgradeable`
`apt list --installed`

## Clean system

`sudo apt autoremove`

