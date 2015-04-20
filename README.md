<img src="http://www.elao.com/images/corpo/logo_red_small.png"/>

# Ansible Role: gem

This role will assume the setup of ruby gems.

It's part of the ELAO [Ansible stack](http://ansible.elao.com) but can be used as a stand alone component.

## Requirements

- Ansible 1.7.2+

## Dependencies

None.

## Installation

Using ansible galaxy:

```bash
ansible-galaxy install elao.gem
```
You can add this role as a dependency for other roles by adding the role to the meta/main.yml file of your own role:

```yaml
dependencies:
  - { role: elao.gem }
```

## Role Variables

| Name                | Default | Type  | Description       |
| ------------------- | ------- | ----  | ----------------- |
| `elao_gem_packages` | [ ]     | Array | Ruby gems list    |

### Configuration example

```yaml
elao_gem_packages:
  - name:          sass
    version:       ~> 3.4
    user_install:  false
```

## Example playbook

    - hosts: servers
      roles:
         - { role: elao.gem }

# Licence

MIT

# Author information

ELAO [**(http://www.elao.com/)**](http://www.elao.com)
