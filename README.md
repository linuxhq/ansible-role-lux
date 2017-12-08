# ansible-role-lux

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-lux.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-lux)

RHEL/CentOS - Lux YUM repository

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    lux_pkg: lux-release
    lux_rel: "{{ ansible_distribution_major_version }}"
    lux_repos:
      lux: False

All repositories are disabled by default.

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.lux
          lux_repos:
            lux: True

## License

GPLv3

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
