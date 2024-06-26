# FNE Ansible Role

## Description

Opinionated Ansible role to install the DVM Project FNE.

## Requirements

Debian or Ubuntu based system, `apt`, and an AMD64, ARM64 or ARM32 CPU.

## Role Variables

| Variable | Description | Default | Required |
|----------|-------------|---------|----------|
| `install` | Set this variable to install/reinstall the DVM Project FNE to the host. This might be useful to turn off if you use the role to regenerate the configs. | `true` | No |
| `use_netbird` | Set this to true if Netbird is installed on the host | `false` | No |
| `dvm_folder` | Set this variable to use a custom folder name throughout the role | `dvm` | No |
| `dvmprov` | Set this variable to install the DVM Provisioning Manager to the FNE host | `true` | No |
| `rebuild` | Set this variable to force a rebuild using the GitHub action.  Rebuild will happen if the `dvmhost` project had changes since the last action run. *GitHub token is mandatory.* | `false` | No |
| `force_rebuild` | Set this variable to force the GitHub action to rebuild, regardless of whether the `dvmhost` project had changes since the last action run.  **`rebuild` *must* be set to `true` for this variable to be considered.** *GitHub token is mandatory.* | `false` | No |

## Limitations

It is **highly recommended** to set `install` to `true` if you make configuration changes, as it is possible the underlying binary has had changes.

## Example Playbook

Please refer to the CANTACS [ansible-deploy repo](https://github.com/CANTACS/ansible-deploy/) for a detailed playbook.
