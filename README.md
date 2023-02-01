# Arch post-install with Ansible
Using Ansible to make post-install configuration of Arch Linux because I can

## Pre-requirements

```bash
sudo pacman -S core/openssh community/ansible community/sshpass
sudo systemctl enable --now sshd
```

```bash
mkdir -p ~/.ssh/
ssh-keyscan 127.0.0.1 >> ~/.ssh/known_hosts
```

## How to use?

```bash
ansible-playbook playbooks/<playbook.yml>  -u <USER> -i inventory/hosts --ask-pass --ask-become-pass
```

Recommended installation order:
- `ansible.yml`
- `add-aura-user.yml`
- `other playbooks`
