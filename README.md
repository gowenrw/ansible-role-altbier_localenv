# Ansible role altbier_localenv

This role will update a linux vm to provide a local environment based on preferences set by variables

## Requirements

This role is known to work with following distributions: 
*  CentOS Stream 9
*  Rocky 9
*  RHEL 9
*  Ubuntu 23.04

## Role Variables

These are defined in [defults/main.yml](defults/main.yml) and [vars/main.yml](vars/main.yml)

These boolean variables control what the role will do:
* altbier_localenv_custom_color_prompt ```default is true```
* altbier_localenv_epel_install ```default is true - ignored on Ubuntu```
* altbier_localenv_pkg_update ```default is true```
* altbier_localenv_pkgs_qol_install ```default is true```
* altbier_localenv_pkgs_build_install ```default is false```
* altbier_localenv_pkgs_putty_install ```default is false```
* altbier_localenv_pkgs_ansible_install ```default is false```
* altbier_localenv_resize_disk ```default is false```
* altbier_localenv_resize_az_rhel_lvm_disk ```default is false - only used on Azure RHEL```

## Dependencies

The following collections are used by this role:
*  community.general
*  ansible.posix

## Example Playbook

```yaml
---
- name: Altbier Localenv Playbook
  hosts: all
  vars:
    ##########
    ## By default these are set to True
    ##########
    #
    ## Custom Color Prompt if set to True
    # altbier_localenv_custom_color_prompt: True
    #
    ## Install EPEL if set to True
    # altbier_localenv_epel_install: True
    #
    ## Package Update if set to True
    #altbier_localenv_pkg_update: True
    #
    ## Install Quality of Life Packages if set to True
    # altbier_localenv_pkgs_qol_install: True
    #
    ##########
    ## By default these are set to False
    ##########
    #
    ## Install Build Packages if set to True
    # altbier_localenv_pkgs_build_install: False
    #
    ## Install PuTTy Package from source if set to True
    # altbier_localenv_pkgs_putty_install: False
    #
    ## Install Ansible Packages if set to True
    # altbier_localenv_pkgs_ansible_install: False
    #
    # Resize local VM partition & filesystem if set to True
    # altbier_localenv_resize_disk: False
    #
    # Resize LVM & filesystem on RHEL in Azure if set to True
    # altbier_localenv_resize_az_rhel_lvm_disk: False
    #
  tasks:
  - name: Import role altbier_localenv
    ansible.builtin.import_role:
      name: gowenrw.altbier_localenv
```

[altbier_localenv.example_playbook.yml](altbier_localenv.example_playbook.yml)

## License

MIT

## Author Information

Written by Richard Gowen (a.k.a. @alt_bier)
