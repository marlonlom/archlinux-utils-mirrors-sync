# archlinux-utils-mirrors-sync
Bash script that retrieves Latest Mirror List Using Reflector In Arch Linux


## Inspiration
This script is based on the contents of the following blog post:

Retrieve Latest Mirror List Using Reflector In Arch Linux, Written by Sk, Published: June 10, 2021. [(Link to blog post)](https://ostechnix.com/retrieve-latest-mirror-list-using-reflector-arch-linux/)


## Prerequisites

* Operative Systems: Linux (Arch linux, exactly)
* Packages (from archlinux wiki):
  - reflector (https://wiki.archlinux.org/title/Reflector)
  - rsync (https://wiki.archlinux.org/title/rsync)
  - curl (https://wiki.archlinux.org/title/curl)


## Usage
(1) Download / Clone the repository using Git.

(2) Navigate to the downloaded repository root folder.

(3) Copy the .config/marlonlom folder and put that into the .config/marlonlom folder of the home directory.
_Note_: In case dont exists the .config directory, you must create it.

```
(inside root folder of the repository once downloaded)
cp -R .config/marlonlom ~/.config/marlonlom

(using rsync -pls check if rsync is installed first before using this-)
rsync -avh .config/marlonlom/ ~/.config/marlonlom/

```

(4) navigate to _~/.config/marlonlom/archlinux/utils_ folder and set execution permissions to _sync-current-mirrors.sh_ file. 

```
# Adds execution privilege the current owner user of the specified file
cd ~/.config/marlonlom/archlinux/utils
chmod -x sync-current-mirrors.sh

# or
chmod -x ~/.config/marlonlom/archlinux/utils/sync-current-mirrors.sh

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
