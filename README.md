teleport
=========

Role for teleport service installation.

Role Variables
--------------

To do

Example Playbook
----------------
```
- hosts: servers
  become: yes
  gather_facts: yes

  vars:
    teleport_version: "16.4.2"
    teleport_proxy_server: "teleport.example.com:443"
    teleport_auth_token: "token"
    teleport_ssh_service_config: |
      enabled: "yes"
    teleport_db_service_config: |
      enabled: "yes"
      databases:
      - name: "mysql-prod"
        description: "Production mysql database"
        protocol: "mysql"
        uri: "10.0.1.26:3306"

  roles:
    - teleport
```

