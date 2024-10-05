# termux.config

#### prerequisite

- [termux v0.118.1](https://github.com/termux/termux-app/releases/download/v0.118.1/termux-app_v0.118.1+github-debug_universal.apk)

---

#### setup

```bash
pkg update && pkg upgrade

pkg install proot-distro openssh syncthing neofetch

proot-distro install debian
proot-distro login debian

apt update && apt upgrade

apt install adduser sudo

adduser kyaruwo
sudo sed -i "/^root/a\kyaruwo ALL=(ALL:ALL) ALL\n" /etc/sudoers

logout

sshd
passwd
pkill sshd

exit 0
```

---

#### ssh

```bash
sshd
```

---

#### syncthing

```bash
proot-distro login --user kyaruwo
syncthing
```

---

#### neofetch

```bash
proot-distro login --user kyaruwo
neofetch
logout
neofetch
```
