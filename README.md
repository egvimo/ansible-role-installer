# Installer

[![Molecule Test](https://github.com/egvimo/ansible-role-installer/actions/workflows/molecule-test.yml/badge.svg)](https://github.com/egvimo/ansible-role-installer/actions/workflows/molecule-test.yml)

> This role includes tasks to setup my personal systems and is designed according to my preferences. It's not meant to be a universal tool, but you can use it as inspiration for your own playbooks.

Ansible role to dynamically install different software from different sources.

This role contains the following custom install tasks:

- Brave Browser
- Google Chrome
- kubectl
- Starship
- Syncthing
- Visual Studio Code

If the package is not one of the above, then the `apt` package manager (`scoop` for Windows hosts) is used to install the package.

## Usage

```yml
- hosts: servers
  roles:
    - role: egvimo.installer
      vars:
        installer_packages:
          - kubectl
          - screen
          - starship
```

## License

Copyright © 2021 egvimo.

Licensed under the MIT License. See [LICENSE](LICENSE).
