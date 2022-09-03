# Arch post-install with Ansible
Using Ansible to make post-install configuration of Arch Linux because I can

How to use?

```bash
ansible-playbook playbooks/<playbook.yml>  -u <USER> -i inventory/hosts --ask-pass --ask-become-pass
```

Recommended installation order:
- `ansible.yml`
- `add-aura-user.yml`
- `other playbooks`
