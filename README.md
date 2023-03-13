# Ansible playbooks for home lab management

- manage.yml
  - Runs all playbooks *other* than performing package updates
- manage_and_update.yml
  - Runs all playbooks, including package updates
- configs.yml
  - Ensures some basic config accuracy, such as DNS configs. 
- dotfiles.yml
  - Pulls my [dotfiles](https://github.com/maclarel/dotfiles) and pushes them out to all managed systems for quality of life.
- packages.yml
  - Ensures specific packages are installed on all managed systems
- update.yml
  - Runs updates for all packages on managed systems
