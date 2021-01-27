## Description
ansible role that used to sync git repos.
For example, sync from github to gitlab.

## ansible playbook example
```bash
---
- name: Mirror Git repos with Ansible
  hosts: localhost
  vars:
    git_dir: "{{playbook_dir}}"
    repo_name: test-git
    branches:
      - master
      - dev
    source_url: 'your source git repo url here!'
    dest_url: 'your destination git repo url here'
  roles:
    - terryzwt.ansible_role_git_repo_sync
```
