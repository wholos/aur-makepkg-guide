# aur-makepkg-guide
Guide for makepkg and PKGBUILD (in archlinux!)

in the directory with PKGBUILD you need to run!

1. ssh-keygen =f ~/.ssh/aur
2. git config --global user.name "YOUR REAL NAME IN AUR" | git config --global user.email "YOUR EMAIL SPECIFIED IN AUR"
3. vim ~/.ssh/config
(IN CONFIG!)
```
Host aur.archlinux.org
    IdentityFile ~/.ssh/aur
    User aur
```
(COPY CONTENT FROM ```~/.ssh/aur.pub``` TO YOUR ACCOUNT ON AUR, IN SSH PUBLICK KEY) 
4. git clone ssh://aur@aur.archlinux.org/NAME_PKG.git
5. makepkg --printsrcinfo > .SRCINFO
6. mv PKGBUILD .SRCINFO NAME_PKG/
(that is, all files)
7. cd NAME_PKG/
8. git add PKBUILD .SRCINFO
(that is, all files)
9. git commit -m "Vesrion 1"
10. git push

all, package in AUR
