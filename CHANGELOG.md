# [CHANGELOG](http://keepachangelog.com/)
All notable changes to this project will be documented in this file.
This project adheres to [Semantic Versioning](http://semver.org/).

## [Unreleased]
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

[unreleased]: https://github.com/ajgarlag/ansible-bootstrap/compare/0.1.0...master
