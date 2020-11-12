
![Ansible Lint](https://github.com/tenantcloud/ansible-role-create-user/workflows/Ansible%20Lint/badge.svg?branch-master)
![Yaml Lint](https://github.com/tenantcloud/ansible-role-create-user/workflows/Yaml%20Lint/badge.svg?branch-master)

tenantcloud.create_user
=========

Ansible role for creating sudo users for servers

  - tenantcloud_create_user

Requirements
------------

Role Variables
--------------

ansible_user: "ubuntu"
sudo_users: "list of users"
user_groups: "dictionary of groups"

Dependencies
------------

Example Playbook
----------------

```yaml
- hosts: localhost
  become: yes
  vars:
    ansible_user: "ubuntu"
    sudo_users:
      - username: "user1"
      - username: "user2"
      - username: "user3"
    user_groups: [ 'sudo', 'ubuntu', 'adm' ]
  roles:
    - tenantcloud.create_user
```

License
-------

BSD

Author Information
------------------

TenantCloud DevOps Team
