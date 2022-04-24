# archlinux-utils-mirrors-sync
Bash script that retrieves Latest Mirror List Using Reflector In Arch Linux


## Inspiration
This script is based on the contents of the following blog post:

Retrieve Latest Mirror List Using Reflector In Arch Linux, Written by Sk, Published: June 10, 2021. [(Website)](https://ostechnix.com/retrieve-latest-mirror-list-using-reflector-arch-linux/)


## Prerequisites

* Operative Systems: Linux (Arch linux, exactly)
* Packages (from archlinux wiki):
  - reflector (https://wiki.archlinux.org/title/Reflector)
  - rsync (https://wiki.archlinux.org/title/rsync)
  - curl (https://wiki.archlinux.org/title/curl)


## Usage
(1) Download / Clone the repository using Git.

(2) Navigate to the downloaded repository root folder.

(3) Copy the .config folder and put that into the .config folder of the home directory.
_Note_: In case dont exists the .config directory, you must create it.

```bash
(inside root folder of the repository once downloaded)
cp .config/marlonlom/archlinux/utils/sync-current-mirrors.sh ~/.config
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
