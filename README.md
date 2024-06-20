Lighthouse VK
=========

LightHouse is a lightweight GUI interface for ClickHouse.

Requirements
------------
- OS Fedora 37 on managed nodes.
- Nginx on managed nodes.

Role Variables
--------------
No variables used.

Templates
--------------
lighthouse.conf.j2 - configuration file for proper work with nginx.

Dependencies
------------
List of roles required for full-time work:
- [Clickhouse](https://github.com/AlexeySetevoi/ansible-clickhouse.git)
- [Vector-role](https://github.com/reocoker85/vector-role.git)
- [Nginx-role](https://github.com/reocoker85/nginx-role.git)


Example Playbook
----------------

Install role :

- Create file ```requirements.yml``` with:
```yaml
- src: git@github.com:reocoker85/lighthouse-role.git      
  scm: git
  version: "main"
  name: lighthouse-role
```
- use command ```ansible-galaxy install -r requirements.yml -p roles``` for downloading role in directory roles.

Use role ( playbook example):

```yaml
- name: Install lighthouse
  hosts: lighthouse
  become: true
  roles:
    - lighthouse-role
  tags: lighthouse
```

Author Information
------------------

### KIG
