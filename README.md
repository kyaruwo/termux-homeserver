# termux.config

<br />

#### prerequisite

- [termux v0.118.1](https://github.com/termux/termux-app/releases/download/v0.118.1/termux-app_v0.118.1+github-debug_universal.apk)

<br />

## init

```bash

pkg update && pkg upgrade

pkg install proot-distro openssh syncthing neofetch

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

sudo sed -i "/^root/a\kyaruwo ALL=(ALL:ALL) ALL" /etc/sudoers

logout

```

```bash

sshd
passwd

```

```bash

pkill sshd

logout

```

<br />

## ssh

- host

```bash
sshd
```

- client

```bash
ssh -p 8022 host_ipaddress
```

<br />

## syncthing

```bash
proot-distro login debian --user kyaruwo
```

```
syncthing
```

<br />

## neofetch

```bash
neofetch
```
