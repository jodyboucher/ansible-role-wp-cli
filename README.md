# Ansible role: wp-cli

An [Ansible](https://www.ansible.com/) role that installs WP-CLI (a set of command-line tools for managing WordPress installations).

## Requirements

None.

## Role Variables

The available variables of this role are listed here along with default values:

```yml
# The WP-CLI version to install
wp_cli_version: 1.1.0

# The directory to write the WP-CLI phar into
wp_cli_bin_path: /usr/local/bin/wp

# The path/filename to write WP-CLI shell tab completions to
wp_cli_completion_dest: /etc/bash_completion.d/wp-completion.bash
```

## Dependencies

None.

## Example Playbook

```yml
---
- hosts: wordpress-servers
  become: true
  vars_files:
    - vars/main.yml
  roles:
    - { role: wp-cli }
```

Inside `vars/main.yml`:

```yml
---
wp_cli_version: 1.1.0
```

## Installation

On the command-line:

```bash
ansible-galaxy install git+https://github.com/jodyboucher/ansible-role-wp-cli.git
```

or in a role file (requirements.yml):

```yml
- name: wp-cli
  src: https://github.com/jodyboucher/ansible-role-wp-cli
  version: master
```

## License

MIT

## Author Information

This role was created by [Jody Boucher](https://jodyboucher.com/).
