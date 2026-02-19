# Fpac

## Setup
fpac searches in `/etc/fpac/` for a file named `main.repo`, so you have to do the following:
```
sudo mkdir /etc/fpac
sudo cp /path/to/main.repo /etc/fpac/
```
Once fpac is set up you can run `fpac --help` for a list of commands.

## Configuring `main.repo`
Since it's just a JSON file you can add your package names to `packages` and the link to the file to `sources`\
*NOTE: fpac installs all packages to /usr/bin/ as to not mess with /bin*

## Updating
To update a package, just run `fpac install package`

## Info
`fpac` relies on both [colorama](https://github.com/tartley/colorama) and [webchk](https://github.com/srfluff/webchk)
