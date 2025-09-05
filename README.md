# unpacman
### the undo button for pacman

**unpacman** is a tool for Arch Linux and Arch-based distributions that completely removes packages installed with pacman, includes all dependencies, extra files, logs, configuration, metadata and essentially everything that entered on you machine with the package installed with pacman ensuring that you undo the pacman command.

## Features
- Full removal of packages installed via pacman
- Tracks all changes for a clean uninstall
- Simple, familiar and Arch-focused

## How does it work
When you call pacman command to install a package, trought hooks system a Transaction ID is attached to all files that comes with the package so the programs gets the location of all files that entered your machine with the package, that way it knows exactly where are the files, size of the files and data types ensuring that when you delete them, everything on your system works as if you never installed a package.