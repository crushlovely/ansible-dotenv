# Ansible role to Transfer a Dotenv File

[![Build Status](http://img.shields.io/travis/crushlovely/ansible-dotenv.svg?style=flat)](https://travis-ci.org/crushlovely/ansible-dotenv)
[![Current Version](http://img.shields.io/github/release/crushlovely/ansible-dotenv.svg?style=flat)](https://galaxy.ansible.com/list#/roles/1180)

This Ansible role transfers dotenv files to servers running an application.

## Installation

``` bash
$ ansible-galaxy install crushlovely.dotenv
```

## Variables

``` yaml
server_env
app_path:
```
You can also add a vars folder to your project folder and have your variables served by adding them to a file and calling it in your playbook.

```yaml
- hosts: localhost
...
  vars_files:
    - vars/default_vars.yml
...
```

## Usage

Once this role is installed on your system, include it in the roles list of your playbook.

``` yaml
- hosts: localhost
  roles:
    - { role: crushlovely.dotenv }
```

## Dependencies

None

## License

MIT