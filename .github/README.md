# ans_role_config_calibre

Install and configure the calibre ebook management application.

[![Release](https://img.shields.io/github/release/digimokan/ans_role_config_calibre.svg?label=release)](https://github.com/digimokan/ans_role_config_calibre/releases/latest "Latest Release Notes")
[![License](https://img.shields.io/badge/license-MIT-blue.svg?label=license)](LICENSE.md "Project License")

## Table Of Contents

* [Purpose](#purpose)
* [Supported Operating Systems](#supported-operating-systems)
* [Quick Start](#quick-start)
    * [Use From Playbook](#use-from-playbook)
* [Role Options](#role-options)
* [Contributing](#contributing)

## Purpose

* Install the [calibre](https://calibre-ebook.com/) ebook management
  application.

## Supported Operating Systems

* Ubuntu
* Arch Linux
* FreeBSD

## Quick Start

### Use From Playbook

1. Create `requirements.yml` in ansible project root, and add this content:

   ```yaml
   # requirements.yml
   - src: https://github.com/digimokan/ans_role_config_calibre
   ```

2. From the project root directory, install/download the role:

   ```shell
   $ ansible-galaxy install --role-file requirements.yml --roles-path ./roles --force-with-deps
   ```

   * _NOTE:_ `--force-with-deps` _ensures subsequent calls download updates_

3. Include the role like any local role, from the project playbook:

   ```yaml
   # playbook.yml
   - hosts: localhost
     connection: local
     tasks:
       - name: "Install and configure the calibre ebook management application"
         ansible.builtin.include_role:
           name: ans_role_config_calibre
         vars:
           calibre_user_name: "user2"
   ```

## Role Options

Vars that must be defined when including the role in the playbook:

  * [dependencies](../defaults/main/dependencies/commands.yml)

Vars with default values, which can be overridden in the playbook:

  * [overridable](../defaults/main/overridable)

## Contributing

* Feel free to report a bug or propose a feature by opening a new
  [Issue](https://github.com/digimokan/ans_role_config_calibre/issues).
* Follow the project's [Contributing](CONTRIBUTING.md) guidelines.
* Respect the project's [Code Of Conduct](CODE_OF_CONDUCT.md).

