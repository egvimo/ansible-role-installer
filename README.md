# Installer

[![Molecule Test](https://github.com/egvimo/ansible-role-installer/actions/workflows/molecule-test.yml/badge.svg)](https://github.com/egvimo/ansible-role-installer/actions/workflows/molecule-test.yml)

> This role includes tasks to setup my personal systems and is designed according to my preferences. It's not meant to be a universal tool, but you can use it as inspiration for your own playbooks.

Ansible role to dynamically install different software from different sources.

This role contains the following custom install tasks:

- bat
- Brave Browser
- Google Chrome
- Docker
- kubectl
- Starship
- Syncthing
- Vagrant
- Visual Studio Code

If the package is not one of the above, then the `apt` package manager (`scoop` for Windows hosts) is used to install the package.

## Installation

The latest version of the role can be installed via Ansible Galaxy:

```shell
ansible-galaxy install egvimo.installer
```

Or directly from the repository via `requirements.yml`:

```yml
roles:
  - name: egvimo.installer
    src: git+https://github.com/egvimo/ansible-role-installer.git
    version: main # Or any other Git branch, tag or commit
```

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
