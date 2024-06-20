# FNE Ansible Role

## Description

Opinionated Ansible role to install the DVM Project FNE.

## Requirements

Debian or Ubuntu based system, `apt`, and an AMD64, ARM64 or ARM32 CPU.

## Role Variables

| Variable | Description | Default | Required |
|----------|-------------|---------|----------|
| install | Set this variable to install/reinstall the DVM Project FNE to the host. This might be useful to turn off if you use the role to regenerate the configs. | true | No |
| use_netbird | Set this to true if Netbird is installed on the host | false | No |
| dvm_folder | Set this variable to use a custom folder name throughout the role | dvm | No |
| dvmprov | Set this variable to install the DVM Provisioning Manager to the FNE host | true | No |

## Example Playbook

Please refer to the CANTACS dvm-deploy repo for a detailed playbook.
