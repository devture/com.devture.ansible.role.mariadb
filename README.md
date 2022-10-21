# MariaDB (MariaDB) Ansible role

This is an [Ansible](https://www.ansible.com/) role which installs [MariaDB](https://mariadb.com/) to run as a [Docker](https://www.docker.com/) container wrapped in a systemd service.

This role *implicitly* depends on [`com.devture.ansible.role.systemd_docker_base`](https://github.com/devture/com.devture.ansible.role.systemd_docker_base).

## Usage

Example playbook:

```yaml
- hosts: servers
  roles:
    - role: galaxy/com.devture.ansible.role.systemd_docker_base

    - when: my_playbook_mariadb_installation_enabled | bool
      role: galaxy/com.devture.ansible.role.mariadb

    - role: another_role
```
