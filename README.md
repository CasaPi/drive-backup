# Google-Drive

Source: https://github.com/odeke-em/drive

## Installation

* Install *go* package:
```
$ sudo pacman -S go
$ cat << ! >> ~/.bashrc
> export GOPATH=\$HOME/gopath
> export PATH=\$GOPATH:\$GOPATH/bin:\$PATH
> !
$ source ~/.bashrc
```

* Install *drive* package:
```
$ go get -u github.com/odeke-em/drive/cmd/drive
```

* Test:
```
~/gopath/bin/drive
```

## Convenient

* In sudo mode:
```
$ mv gopath /opt/.
$ chown root -R /opt/gopath
$ chgrp root -R /opt/gopath
$ chmod +x /opt/gopath/bin/drive
```
* Finally:
```
$ echo "alias drive='/opt/gopath/bin/drive'" >> ~/.bashrc
```

## Initialization

```
$ mkdir gdrive
$ cd gdrive
$ drive init
```

## Pull & Push

More or less same principe than GIT:
```
$ drive [pull|push] <files> <directories>
$ drive [pull|push] -h (help)
```

Prevent to overwriting of old content:
```
$ drive [push|pull] -no-clobber
```
