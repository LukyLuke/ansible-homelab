# Ansible Scripts for my HomeLAB

Proxmox on a Beelink

## Setup a Debian/Ubuntu VM/Container

```bash
apt update
apt full-upgrade
apt install sudo
adduser -U -s /bin/bash -m -G users ansible
echo "ansible ALL=(ALL:ALL) NOPASSWD: ALL" /etc/sudoers.d/ansible
chmod 0600 /etc/sudoers.d/ansible
mkdir -p ~ansible/.ssh
echo "ENTER_YOUR_SSH_PUB_KEY_HERE" > ~ansible/.ssh/authorized_keys
chown -R ansible:ansible ~ansible/.ssh
chmod 0600 ~ansible/.ssh/authorized_keys
chmod 0700 ~ansible/.ssh
passwd ansible
```
