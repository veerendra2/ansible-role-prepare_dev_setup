# Ansible Role: `prepare-dev-setup`
An ansible role to install necessary packages and configure my Ubuntu and MacOS.

<img src="https://user-images.githubusercontent.com/8393701/248329468-ed036c98-08e7-4ee6-99ef-d5cef2e48a95.png" alt="Windows" width="70"/> <img src="https://user-images.githubusercontent.com/8393701/248331160-ae1cd8f6-7c4b-483b-9799-6b44ed3f30f2.png" alt="Mac" width="74"/>

## Usage
```yaml
- hosts: all

  roles:
    - veerendra2.prepare-dev-setup
```
### Variables
```yaml
enable_docker_swarm_metrics: false
enable_docker_live_restore: true
enable_userns_remap: false
enable_docker_swarm_mode: false
docker_swarm_advertise_addr: ""

# clone your git repos
git_projects:
  dotfiles: "git@github.com:veerendra2/dotfiles.git"

github_username_keys: "https://github.com/veerendra2.keys"

# this option will install dotfiles from https://github.com/veerendra2/dotfiles.git
install_dotfiles: true
```