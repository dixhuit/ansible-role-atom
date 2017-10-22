# Ansible role: Atom

[![Build Status](https://travis-ci.org/danbohea/ansible-role-atom.svg?branch=master)](https://travis-ci.org/danbohea/ansible-role-atom)

Installs and configures [Atom](https://atom.io) on macOS.

- Installs Atom (via Homebrew Cask).
- Installs Atom packages.
- Copies config into place.
- Upgrades existing Atom packages if desired.


## Requirements

- macOS 10.11 or 10.12


## Role Variables

All role default variables are listed below along with their respective default values.

```yaml
# Whether to upgrade existing packages whenever this role runs.
atom_upgrade_packages: false

# List of Atom packages to install.
# Values must be apm package names.
# Fill yer boots: https://atom.io/packages
atom_packages: []
```


## Dependencies

- [danbohea.homebrew](https://galaxy.ansible.com/danbohea/homebrew)


## Example Playbook

```yaml
- hosts: localhost
  connection: local

  roles:
    - danbohea.ansible-role-atom
```


## License

MIT


## Author Information

This role was created by [Dan Bohea](http://bohea.co.uk) primarily for use with [Macsible](https://github.com/macsible/macsible).
