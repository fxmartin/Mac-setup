# Homebrew Cask

Let's see if we can get the elegance, simplicity, and speed of Homebrew for the installation and management of GUI Mac applications such as Google Chrome and Adium.

### Install

As of December 2015, cask comes installed with Homebrew directly.

    $ brew cask install google-chrome

### Search

It is really simple to check if the app is supported by cask by going to the search page on [caskroom.io](http://caskroom.io/) or entering the following instruction on the command line :

    $ brew cask search avira

### Base applications installation

Install the following base applications :
```
$ brew cask install google-chrome
$ brew cask install xquartz
$ brew cask install istat-menus
$ brew cask install iterm2
$ brew cask install dropbox
$ brew cask install avira-antivirus
```

### Quick look plugins

Some [plugins](https://github.com/sindresorhus/quick-look-plugins) to enable different files to work with Mac Quicklook. Includes features like syntax highlighting, markdown rendering, preview of jsons, patch files, csv, zip files etc.

    $ brew cask install qlcolorcode
    $ brew cask install qlstephen
    $ brew cask install qlmarkdown
    $ brew cask install quicklook-json
    $ brew cask install qlprettypatch
    $ brew cask install quicklook-csv
    $ brew cask install betterzipql
    $ brew cask install webpquicklook
    $ brew cask install suspicious-package

### App Installation

I'll now cover installation of the apps that I have mentioned in the apps section using cask.

```
$ brew cask install atom
$ brew cask install firefox
$ brew cask install vlc
$ brew cask install microsoft-office
$ brew cask install vmware-fusion
$ brew cask install alfred
$ brew cask install 1password
$ brew cask install sublime-text
```
