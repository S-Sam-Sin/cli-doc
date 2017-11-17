# cli-doc.github.io
My personal Linux Command-Line / Bash cheat sheet.

##Package Handling

######All around installation.
Install applications from PPA ([Personal Package Archive](https://en.wikipedia.org/wiki/Ubuntu_(operating_system)#Package_Archives)) :

![alt text](https://img.shields.io/badge/user-root-red.svg) ![alt text](https://img.shields.io/badge/user-sudo-green.svg)
```
sudo apt install <package>
```

```
sudo aptitude install <package>
```
Install applications from repository (PIP) :

![alt text](https://img.shields.io/badge/user-root-red.svg) ![alt text](https://img.shields.io/badge/user-sudo-green.svg)

1.Python 2x
```
pip install <package>
```
2.Python 3x
```
pip3 install <package>
```
Install applications from `Debian package`:

![alt text](https://img.shields.io/badge/user-root-red.svg) ![alt text](https://img.shields.io/badge/user-sudo-green.svg)

1.chain method
```
cd <directory url of debian package> && sudo dpkg -i ./<file name of debian package>.deb
```
2.direct method
```
sudo dpkg -i ./<directory url of debian package>/<file name of debian package>.deb
```
Install failed :

![alt text](https://img.shields.io/badge/user-root-red.svg) ![alt text](https://img.shields.io/badge/user-sudo-green.svg)
```
sudo apt --purge autoremove <failed package> && sudo dpkg --configure -a && sudo apt update && sudo aptitude install <failed package>
```
######Updating application.

Updating system :

![alt text](https://img.shields.io/badge/user-root-red.svg) ![alt text](https://img.shields.io/badge/user-sudo-green.svg)
```
sudo apt update && sudo apt upgrade && sudo apt --purge autoremove
```
```
sudo aptitude update && sudo aptitude upgrade && sudo apt --purge autoremove
```
Troubleshoot updating:

![alt text](https://img.shields.io/badge/user-root-red.svg) ![alt text](https://img.shields.io/badge/user-sudo-green.svg)
```
sudo dpkg --configure -a
```
######Uninstall application.

Remove applications :

![alt text](https://img.shields.io/badge/user-root-red.svg)

1.standard.
```
sudo apt remove <package>
```
2.removing config files & linked unused libraries.
```
sudo apt --purge autoremove <package>
```
3.advanced uninstall with multiple situations.
```
sudo aptitude remove <package>
```
##Trick & Tips

Bypass spaces in names.

![alt text](https://img.shields.io/badge/user-root-red.svg) ![alt text](https://img.shields.io/badge/user-sudo-green.svg) ![alt text](https://img.shields.io/badge/user-normal-blue.svg)

example to cd in a directory named `My Directory`.
```
cd /home/Sayid/My\ Directory/
```
Become `root`:

![alt text](https://img.shields.io/badge/user-sudo-green.svg)
```
sudo su
```
##Command-Line applications

Ranger - File Manager
![alt text](./screenshots/ranger.png)
```
sudo apt install ranger
```
Glances - System Monitor
![alt text](./screenshots/glances.png)
```
sudo apt install glances
```
##Deprecated Commands

Replaced by `apt`

![alt text](https://img.shields.io/badge/user-root-red.svg) ![alt text](https://img.shields.io/badge/user-sudo-green.svg)

```
apt-get
```