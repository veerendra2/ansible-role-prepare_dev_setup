# Ansible Role: `prepare_dev_setup`

[![Release](https://github.com/veerendra2/ansible-role-prepare_dev_setup/actions/workflows/release.yml/badge.svg)](https://github.com/veerendra2/ansible-role-prepare_dev_setup/actions/workflows/release.yml)
[![Lint and Test](https://github.com/veerendra2/ansible-role-prepare_dev_setup/actions/workflows/tests.yml/badge.svg)](https://github.com/veerendra2/ansible-role-prepare_dev_setup/actions/workflows/tests.yml)
![Ansible Role](https://img.shields.io/ansible/role/d/63075)
![Ansible Galaxy Role Name](https://img.shields.io/ansible/role/63075)
![GitHub release (release name instead of tag name)](https://img.shields.io/github/v/release/veerendra2/ansible-role-prepare_dev_setup?include_prereleases&style=plastic)

An ansible role to install necessary packages and configure my Ubuntu and macOS.

<img src="https://user-images.githubusercontent.com/8393701/248329468-ed036c98-08e7-4ee6-99ef-d5cef2e48a95.png" alt="Windows" width="70"/> <img src="https://user-images.githubusercontent.com/8393701/248331160-ae1cd8f6-7c4b-483b-9799-6b44ed3f30f2.png" alt="Mac" width="74"/>

| OS                   | Architecture     | Tested             |
| -------------------- | ---------------- | ------------------ |
| `Ubuntu 22.04.3 LTS` | `arm64`, `amd64` | :white_check_mark: |
| `macOS 14.0`         | `arm64`          | :white_check_mark: |

## Usage

> Example: [veerendra2/prepare-my-machine](https://github.com/veerendra2/prepare-my-machine.git)

```bash
ansible-galaxy install veerendra2.prepare_dev_setup
```

```yaml
---
- hosts: all

  roles:
    - veerendra2.prepare_dev_setup
```

### Dafault variables

```yaml
---
# docker images to be pulled
docker_images:
  - alpine
  - veerendra2/utils:latest

# clone git repos
git_projects: []

# authorized keys from url
public_keys_url: https://github.com/veerendra2.keys

# install dotfiles [https://github.com/veerendra2/dotfiles.git]
install_dotfiles: true

# add hosts to ~/.ssh/known_hosts
known_hosts_list:
  - github.com
  - gitlab.com
```
