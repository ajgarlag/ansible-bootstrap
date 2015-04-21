ajgarlag.bootstrap
==================

Ansible role to perform some basic setup to execute other ansible roles.

[![Build Status](https://travis-ci.org/ajgarlag/ansible-bootstrap.svg?branch=master)](https://travis-ci.org/ajgarlag/ansible-bootstrap)

Role Variables
--------------

* **ajgarlag_bootstrap_packages**: Array of packages to install.
* **ajgarlag_bootstrap_ssh_key_user**: User to add the SSH keys (defaults to *ansible_user_id* var).
* **ajgarlag_bootstrap_add_current_user_key**: Boolean flag to control the addition of current user ssh key (defaults to *yes*).
* **ajgarlag_bootstrap_extra_authorized_keys**: Array of extra SSH keys to add.

Example Playbook
----------------

```yml
- hosts: all
  roles:
    - role: ajgarlag.bootstrap
      ajgarlag_bootstrap_ssh_key_user: deploy
```

License
-------

MIT

Author Information
------------------

Developed with ♥ by [Antonio J. García Lagar](http://aj.garcialagar.es).
