altbier_localenv
============

This role will update a linux vm local environment as needed by use case.

Requirements
------------

This role is known to work with following distributions: 
*  CentOS Stream 9
*  Rocky 9
*  RHEL 9
*  Ubuntu 23.04

Role Variables
--------------

These are defined in [defults/main.yml](defults/main.yml) and [vars/main.yml](vars/main.yml)

Dependencies
------------

The following collections are used by this role:
*  community.general
*  ansible.posix

Example Playbook
----------------

[altbier_localenv.example_playbook.yml](altbier_localenv.example_playbook.yml)

License
-------

MIT

Author Information
------------------

Written by Richard Gowen (a.k.a. @alt_bier)
