# Fpac

## Setup
fpac searches in `/etc/fpac/` for a file named `main.repo`, so you have to do the following:
```
sudo mkdir /etc/fpac
sudo cp /path/to/main.repo /etc/fpac/
```
Once fpac is set up you can run `fpac --help` for a list of commands.

## Configuring `main.repo`

`packages`: List of packages available to download\
`sources`: The link to the package file *NOTE: fpac uses WGET under the hood, so name the file the same as the package name*\
`libraries`: Added in 1.1.0, it's a list of available libraries. *NOTE: The user is not allowed to install these manually*\
`LSources`: The link to the library file. *NOTE: fpac will check for a file names {library}.py, not {library}*\
`links`: A list containing lists of libraries to install along with packages. *NOTE: The sub-lists must numerically match the packages*

## Updating
To update a package, just run `fpac install package`

## Info
`fpac` relies on both [colorama](https://github.com/tartley/colorama) and [webchk](https://github.com/srfluff/webchk)
