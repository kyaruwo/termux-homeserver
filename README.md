# termux.config

[termux v0.118.1](https://github.com/termux/termux-app/releases/download/v0.118.1/termux-app_v0.118.1+github-debug_universal.apk)

<br />

## init

```bash

pkg update && pkg upgrade

pkg install proot-distro syncthing neofetch

proot-distro install debian

```

```bash
proot-distro login debian
```

```bash

apt update && apt upgrade

apt install adduser sudo

adduser kyaruwo

```

```bash
sed --in-place "/^root/a\kyaruwo ALL=(ALL:ALL) ALL" /etc/sudoers
```

<br />

## syncthing

```bash
proot-distro login debian --user kyaruwo
```

```bash
syncthing
```

```
http://127.0.0.1:8384
```

<br />

## neofetch

```bash
neofetch
```
