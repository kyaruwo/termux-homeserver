# termux homeserver

<br />

### prerequisite

[termux v0.118.1](https://github.com/termux/termux-app/releases/download/v0.118.1/termux-app_v0.118.1+github-debug_universal.apk)

<br />

<details><summary>installation</summary>

<br />

termux

```bash
pkg update && pkg upgrade
```

distro

```bash
pkg i proot-distro
```

```bash
pd i debian
```

login as root

```bash
pd login debian
```

debian (logged in as root)

```bash
apt update && apt upgrade
```

packages (logged in as root)

```bash
apt install adduser sed sudo openssh-server tmux syncthing neofetch
```

user (logged in as root)

```bash
adduser kyaruwo
```

```bash
sed -i "/^root/a\kyaruwo ALL=(ALL:ALL) ALL" /etc/sudoers
```

```bash
logout
```

autologin as kyaruwo on debian when termux run

```bash
echo -e "\nclear\npd login debian --user kyaruwo" >> /data/data/com.termux/files/usr/etc/bash.bashrc
```

login as kyaruwo

```bash
pd login debian --user kyaruwo
```

ssh (logged in as kyaruwo)

```bash
ssh-keygen
```

```bash
echo -e "\nPort 10122" >> /etc/ssh/sshd_config
```

```bash
echo "HostKey /home/kyaruwo/.ssh/id_rsa" >> /etc/ssh/sshd_config
```

sshd (logged in as kyaruwo)

```bash
mkdir /run/sshd
```

```bash
echo -e "\nalias sshd='sudo /usr/sbin/sshd'" >> ~/.bashrc
```

tmux on ssh (logged in as kyaruwo)

```bash
echo -e '\nif [[ $- =~ i ]] && [[ -z "$TMUX" ]] && [[ -n "$SSH_TTY" ]]; then\n\ttmux new -A -s owo\nfi' >> ~/.bashrc
```

<br />

</details>

<br />

### syncthing

start

```bash
syncthing
```

(web)GUI

```
localhost:8384
```

<br />

### ssh

server

```bash
sshd
```

client

```sh
ssh -p 10122 kyaruwo@ip_address
```

<br />
