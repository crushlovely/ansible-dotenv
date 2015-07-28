# Ansible role to create a .env file

[![Build Status](https://circleci.com/gh/crushlovely/ansible-dotenv.svg?style=shield)](https://github.com/crushlovely/ansible-dotenv)
[![Current Version](http://img.shields.io/github/release/crushlovely/ansible-dotenv.svg?style=flat)](https://galaxy.ansible.com/list#/roles/2454)

This Ansible role creates a [.env](https://github.com/bkeepers/dotenv) file on your servers based on variables you define in your playbook vars.

## Installation

``` bash
$ ansible-galaxy install crushlovely.dotenv,v1.0.0
```

## Variables

``` yaml
dotenv:
  path: "/path/to/your/file" # The folder where your .env will be stored on the server.
  user: "username" # The username of the user assigned permission to the .env file.
  group: "groupname" # The group name of the group assigned permission to the .env file.
  vars:
    rails_env: production
    api_token: s3cr3tt0k3n
```

## Usage

Once this role is installed on your system, include it in the roles list of your playbook.

``` yaml
- hosts: localhost
  roles:
    - crushlovely.dotenv
```

The example YAML above will be transformed into a standard `.env` file like so:

```bash
RAILS_ENV=production
API_TOKEN=s3cr3tt0k3n
```

## Dependencies

None

## License

MIT
