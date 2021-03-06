# [CHANGELOG](http://keepachangelog.com/)
All notable changes to this project will be documented in this file.
This project adheres to [Semantic Versioning](http://semver.org/).

## [Unreleased]

## [0.2.5] - 2021-03-31
 - Clear previous SSH keys

## [0.2.4] - 2020-04-25

### Added
 - Add `logwatch` and `unattended-upgrades` to default packages list
 - Support multivalued rkhunter directives

### Changed
 - Use python3 version of packages

## [0.2.3] - 2016-12-29

### Fixed
- Remove duplicate when key in `aliases.yml` tasks

## [0.2.2] - 2016-12-02

### Changed
- Tasks related to `exim4` are executed before that tasks related to `/etc/aliases`

### Fixed
- Set exim4 configuration type to satellite
- Set `/bin/bash` shell for sudoer user
- Check that `/etc/aliases` exists before to any modification

## [0.2.1] - 2016-05-31

### Added
- Allow to configure mail aliases
- Install rkhunter
- Optional configuration of exim4 with smarthost relay


## [0.2.0] - 2016-05-30

### Added
- Support for ansible 2.0
- Disable by default SSH login with password for root
- Allow to disable SSH password login for all users
- Allow sudoer user creation
- Copy current local user SSH key by default
- Disable SSH password login by default

### Changed
- Renamed `ajgarlag_bootstrap_add_current_user_key` var to `ajgarlag_bootstrap_ssh_authorize_current_user_key`
- Renamed `ajgarlag_bootstrap_extra_authorized_keys` var to `ajgarlag_bootstrap_ssh_extra_authorized_keys`

### Removed
- Drop support for Ubuntu and old Debian distributions
- Drop support for ansible <2.0

## 0.1.0 - 2016-05-27

[unreleased]: https://github.com/ajgarlag/ansible-bootstrap/compare/0.2.5...master
[0.2.5]: https://github.com/ajgarlag/ansible-bootstrap/compare/0.2.4...0.2.5
[0.2.4]: https://github.com/ajgarlag/ansible-bootstrap/compare/0.2.3...0.2.4
[0.2.3]: https://github.com/ajgarlag/ansible-bootstrap/compare/0.2.2...0.2.3
[0.2.2]: https://github.com/ajgarlag/ansible-bootstrap/compare/0.2.1...0.2.2
[0.2.1]: https://github.com/ajgarlag/ansible-bootstrap/compare/0.2.0...0.2.1
[0.2.0]: https://github.com/ajgarlag/ansible-bootstrap/compare/0.1.0...0.2.0
