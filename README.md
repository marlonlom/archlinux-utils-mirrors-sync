# archlinux-utils-mirrors-sync
Bash script that retrieves Latest Mirror List Using Reflector In Arch Linux


## Inspiration
This script is based on the contents of the following blog post:

Retrieve Latest Mirror List Using Reflector In Arch Linux, Written by Sk, Published: June 10, 2021. [(Link to blog post)](https://ostechnix.com/retrieve-latest-mirror-list-using-reflector-arch-linux/)


## Prerequisites

* Have an active Internet connection
* Operative Systems: Linux (Arch linux, exactly)
* Packages (from archlinux wiki):
  - reflector (https://wiki.archlinux.org/title/Reflector)
  - rsync (https://wiki.archlinux.org/title/rsync)
  - curl (https://wiki.archlinux.org/title/curl)


## Preparation
For preparing the script for usage, follow the steps:

A) Download / Clone the repository using Git.

B) Navigate to the downloaded repository root folder.

C) Copy the .config/marlonlom folder and put that into the .config/marlonlom folder of the home directory.
_Note_: In case dont exists the .config directory, you must create it.

```
(inside root folder of the repository once downloaded)
cp -R .config/marlonlom ~/.config/marlonlom

(using rsync -pls check if rsync is installed first before using this-)
rsync -avh .config/marlonlom/ ~/.config/marlonlom/
```

D) navigate to _~/.config/marlonlom/archlinux/utils_ folder and set execution permissions to _sync-current-mirrors.sh_ file. 

```
# Adds execution privilege the current owner user of the specified file
cd ~/.config/marlonlom/archlinux/utils
chmod +x sync-current-mirrors.sh

# or
chmod +x ~/.config/marlonlom/archlinux/utils/sync-current-mirrors.sh
```

### Preparing script alias for better execution
For easy usage of the script, its recommended to make alias and using it for running the script file inside the terminal.


#### Editing *.bashrc* file
Open .bashrc file for editing - in this example, im using nano, but feel free to use another text editor-
```
sudo nano ~/.bashrc
```

Add this at the bottom of .bashrc file
```
# Sync current mirrors
alias sync-current-mirrors="clear && sudo ~/.config/marlonlom/archlinux/utils/sync-current-mirrors.sh"
```

Read and execute updated .bashrc file
```
source ~/.bashrc
```

#### Editing *.zshrc* file
Open .szhrc file for editing - in this example, im using nano, but feel free to use another text editor-
```
sudo nano ~/.zshrc
```

Add this at the bottom of .zshrc file
```
# Sync current mirrors
alias sync-current-mirrors="clear && sudo ~/.config/marlonlom/archlinux/utils/sync-current-mirrors.sh"
```

Read and execute updated .szhrc file
```
source ~/.zshrc
```


## Usage
After preparing the script for its usage, in the terminal, invoke the script by typing the following:

```
$ sync-current-mirrors
```


# License
```
Copyright (C) 2022 marlonlom

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
```
