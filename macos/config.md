
# Configuration

## Hotkeys

`Cmd + Shift + .` Toggles the hidden files in the finder.

## .files

Almost all programs have a `.{programName}` file in `~/` that can be used to configure the app.

## Tags

- Tags can be modified in preferences in the finder `Cmd + ,`

## Terminal

- Add open terminal here command from finder
  - Head into System Preferences and select Keyboard > Shortcuts > Services. Find "New Terminal at Folder" in the settings and click the box. Now, when you're in Finder, just right-click a folder and you're shown the open to open Terminal. When you do, it'll start right in the folder you're in. It's not always necessary, but it's a big help for all those Terminal commands that require a very specific location.

## Visual Studio Code

- `Cmd + Shift + P` shell command install code in path -> will install vsc as the default text editor.

## Git

- Git credentials are put into the osx keychain app by default
- `git config --global` can be found in `~/.gitconfig`

## Install Consolas

``` bash

# Thanks to this post:
# http://blog.ikato.com/post/15675823000/how-to-install-consolas-font-on-mac-os-x

$ brew install cabextract
$ cd ~/Downloads
$ mkdir consolas
$ cd consolas
$ curl -LO https://sourceforge.net/projects/mscorefonts2/files/cabs/PowerPointViewer.exe
$ cabextract PowerPointViewer.exe
$ cabextract ppviewer.cab
$ open CONSOLA*.TTF

```

## Bash profile

https://scriptingosx.com/2017/04/about-bash_profile-and-bashrc-on-macos/

- depending on the terminal, some will load .bash_profile for each terminal session and some will load .bashrc. In linux it's normal to load .bashrc first and on mac it normally load .bash_profile.

put this in .bash_profile

``` bash

# if bashrc exits then load it
if [ -r ~/.bashrc ]; then
   source ~/.bashrc
fi

```

## Add Open with code in finder

- Open Automator 
- File -> New -> Quick Action 
- Change "Service Receives" to "files or folders" in "Finder" 
- Add a "Run Shell Script" action 
- Change "Pass input" to "as arguments" 
- Paste the following in the shell script box: open -n -b "com.microsoft.VSCode" --args "$*" 
- Save it as something like "Open in Visual Studio Code"