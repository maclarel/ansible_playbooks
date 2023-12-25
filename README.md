# Ansible playbooks for home lab management

Run everything useful through a cronjob (or other automation) with:

```
ansible-playbook -i ~/.ansible/inventory ~/.ansible/ansible_playbooks/vm_manage/playbooks/manage_and_update.yml --vault-password-file ~/.ansible/.vault_pass
```

- `manage.yml` (deprecated)
  - Runs all playbooks *other* than performing package updates.
- `manage_and_update.yml`
  - Runs all playbooks, including package updates
- `configs.yml`
  - Ensures some basic config accuracy, such as DNS configs. 
- `dotfiles.yml` (deprecated)
  - Pulls my [dotfiles](https://github.com/maclarel/dotfiles) and pushes them out to all managed systems for quality of life.
- `letsencrypt.yml`
  - Runs a script on the target host to renew Let's Encrypt certs if needed.
- `packages.yml`
  - Ensures specific packages are installed on all managed systems.
- `pihole_custom_list.yml`
  - Enforces `custom.list` hardlink to a version maintained elsewhere.
- `reboot_if_needed.yml`
  - Performs a rolling reboot of servers requiring it after package upgrades.
- `update.yml`
  - Runs updates for all packages on managed systems
- `update_docker_compose.yml`
  - Pulls the latest images for all docker-compose stacks in docker's directory, then prunes containers/images.

