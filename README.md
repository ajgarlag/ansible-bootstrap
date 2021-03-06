ajgarlag.bootstrap
==================

Ansible role to perform some basic setup to execute other ansible roles.

[![Build Status](https://travis-ci.org/ajgarlag/ansible-bootstrap.svg?branch=master)](https://travis-ci.org/ajgarlag/ansible-bootstrap)

Role Variables
--------------

* **ajgarlag_bootstrap_packages**: Array of packages to install.
* **ajgarlag_bootstrap_sudo_sudoer**: When set, the user will be created and added as sudoer (defaults to emtpy string).
* **ajgarlag_bootstrap_sudo_require_password**: Boolean flag to require password authentication for sudoer (defaults to `yes`).
* **ajgarlag_bootstrap_ssh_key_user**: User to add the SSH keys (defaults to `{{ajgarlag_bootstrap_sudo_sudoer}}` var if set, to `ansible_user_id` otherwise.).
* **ajgarlag_bootstrap_ssh_authorize_current_user_key**: Boolean flag to control the addition of current user ssh key (defaults to `yes`).
* **ajgarlag_bootstrap_ssh_extra_authorized_keys**: Array of extra SSH keys to add (defaults to `[]`).
* **ajgarlag_bootstrap_ssh_allow_root_login**: Controls how the root user can make SSH login. Allowed values are `yes`, `no` or `without-password` (defaults to `no`).
* **ajgarlag_bootstrap_ssh_allow_password_login**: Boolean flag to enables SSH password login (defaults to `no`).
* **ajgarlag_bootstrap_ufw_enable**: Boolean flag to control if ufw firewall must be enabled by this role (defaults to `yes`).
* **ajgarlag_bootstrap_rkhunter_directives**: Dictionary of rkhunter configuration directives (by default it only sets `ALLOW_SSH_ROOT_USER` directive).
* **ajgarlag_bootstrap_exim4relay**: Boolean flag to enable exim4 satellite with smarthost relay (defaults to `yes`).
* **ajgarlag_bootstrap_exim4relay_host**: Smarthost name or IP (defaults to empty string).
* **ajgarlag_bootstrap_exim4relay_port**: Smarthost port (defaults to `25`).
* **ajgarlag_bootstrap_exim4relay_credentials**: Dictionary with credentias for smarthost connection (defaults to `{}`, see [defaults/main.yml](defaults/main.yml)).
* **ajgarlag_bootstrap_aliases_to_root**: Array of usernames to alias to root email account (defaults to `[]`).
* **ajgarlag_bootstrap_aliases_root_alias**: Email address where to redirect root emails (defaults to emtpy string).

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
