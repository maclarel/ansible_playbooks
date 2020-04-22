# Ansible playbooks for home lab management

Note that these assume passwordless `sudo` access on the target system(s).

- manage.yml
  - Runs all playbooks *other* than performing package updates
- manage_and_update.yml
  - Runs all playbooks, including package updates
- configs.yml
  - Ensures some basic config accuracy, such as DNS configs. Hyper-V doesn't let host and guests communicate, and my hypervisor also happens to run my DNS (PiHole) in a docker container... so this is problematic.
- dotfiles.yml
  - Pulls my [dotfiles](https://github.com/maclarel/nix) and pushes them out to all managed systems for quality of life.
- packages.yml
  - Ensures specific packages are installed on all managed systems
- update.yml
  - Runs updates for all packages on managed systems
