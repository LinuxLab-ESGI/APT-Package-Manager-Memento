# APT-Package-Manager-Memento

Memento for APT to manage our package.

APT (**A**dvanced **P**ackage **T**ool) is a package manager Debian and Debian's like distros.

Debian distors uses a packaging sytem called **dpkg** (Debian package). It provides programs and applications for installation in the way that we don't have to manually build a program from the source code. There is a dpkg manager but APT is more friendly to use.

>Here we are using `apt` (new way) and not `apt-get` (old way), apt has more advantages over apt-get such as aprogress bar, prompoting the number of package that can be upgraded, simplier commands, etc.

## Update package database

APT works on database of available packages, we have to update the repository of packages to know if thery are newer packages.  
It will check all repository in **/etc/apt/source.list**. It is a command to do before installing or updating a program :

`sudo apt update`

## Update installed packages

Now we can upgrade all installed packages :

`sudo apt upgrade`

We can combine the two commands with `&&`, with `-y` to say yes we want to upgrade all the packages :

`sudo apt update && sudo apt upgrade -y`

We can use `full-upgrade` to let APT remove all the necessary packages :

`sudo apt full-upgrade`

## Install new packages

To install a package :  
`sudo apt install package_name`  
Or multiple packages :  
`sudo apt install packageName <packageName2`

Install without upgrading :  
`sudo apt install packageName --no-upgrade` (Don't want to upgrade if it's installed)

Install only upgrading :  
`sudo apt install packageName --only-upgrade` (Don't want to install if it's not upgradable)

Install with specific version number (the latest is intalled by default) :  
`sudo apt install packageName=versionNumber`

If we downloaded a **.deb** file, we can install it with :  
`sudo dpkg -i fichier.deb`
`sudo apt install -f` (sintalling dependencies)
Or :
`sudo apt install fichier.deb`

## Remove packages

`sudo apt remove packageName` (removes only binaries)  
`sudo apt autoremove` (removes binaries and dependencies if it's not used)  
`sudo apt purge packageName` (removes binaries and files configurations)

## Search for some informations

`apt search packageName` (searhc a package)
`apt show packageName` (search a package by a name or its description)
`apt list --upgradeable`(list upgradable packages)
`apt list --installed` (list installed packages)

## Clean system

`sudo apt autoremove` (removes unused dependencies)
`sudo apt clean` (removes oudated cache)
`sudo apt autoclean` (removes cache)

___
Updated : 12/12/2020
Author : AnthonyF
