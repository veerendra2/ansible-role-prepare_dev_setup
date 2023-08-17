[![Release](https://github.com/veerendra2/ansible-role-prepare_dev_setup/actions/workflows/release.yml/badge.svg)](https://github.com/veerendra2/ansible-role-prepare_dev_setup/actions/workflows/release.yml)
[![Lint and Test](https://github.com/veerendra2/ansible-role-prepare_dev_setup/actions/workflows/tests.yml/badge.svg)](https://github.com/veerendra2/ansible-role-prepare_dev_setup/actions/workflows/tests.yml)
![Ansible Role](https://img.shields.io/ansible/role/d/63075)
![Ansible Galaxy Role Name](https://img.shields.io/ansible/role/63075)
![GitHub release (release name instead of tag name)](https://img.shields.io/github/v/release/veerendra2/ansible-role-prepare_dev_setup?include_prereleases&style=plastic)
# Ansible Role: `prepare_dev_setup`
An ansible role to install necessary packages and configure my Ubuntu and MacOS.

<img src="https://user-images.githubusercontent.com/8393701/248329468-ed036c98-08e7-4ee6-99ef-d5cef2e48a95.png" alt="Windows" width="70"/> <img src="https://user-images.githubusercontent.com/8393701/248331160-ae1cd8f6-7c4b-483b-9799-6b44ed3f30f2.png" alt="Mac" width="74"/>

|    | Tested on |
| -- | --------- |
| :white_check_mark: | `Ubuntu 22.04.3 LTS aarch64` |
| :white_check_mark: | `macOS 13.5 22G74 arm64` |

## Usage
```yaml
- hosts: all

  roles:
    - veerendra2.prepare_dev_setup
```
### Variables
```yaml
---
enable_docker_swarm_metrics: false
enable_docker_live_restore: true
enable_userns_remap: false
enable_docker_swarm_mode: false
docker_swarm_advertise_addr: ""

# clone your git repos
git_projects:
  my-utils: "https://github.com/veerendra2/my-utils.git"
  raspberrypi-homeserver: "https://github.com/veerendra2/raspberrypi-homeserver.git"

github_username_keys: "https://github.com/veerendra2.keys"

# install dotfiles [https://github.com/veerendra2/dotfiles.git]
install_dotfiles: true

# install bettercap [https://www.bettercap.org/]
install_bettercap: true
```
