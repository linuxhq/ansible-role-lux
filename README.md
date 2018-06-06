# ansible-role-lux

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-lux.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-lux)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-lux-blue.svg?style=flat)](https://galaxy.ansible.com/linuxhq/lux)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

RHEL/CentOS - Lux YUM repository

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    lux_disable_plugin: []
    lux_disablerepo: []
    lux_enable_plugin: []
    lux_enablerepo: []
    lux_packages: []
    lux_pkg: lux-release
    lux_rel: "{{ ansible_distribution_major_version }}"
    lux_repository_lux: false

All repositories are disabled by default.

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.lux
          lux_disable_plugin:
            - post-transaction-actions
          lux_enablerepo:
            - epel
          lux_packages:
            - jailkit
          lux_repository_lux: true

## License

Copyright (C) 2018 Taylor Kimball <tkimball@linuxhq.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
