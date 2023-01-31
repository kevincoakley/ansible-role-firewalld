ansible-role-firewalld
======================

![](https://github.com/kevincoakley/ansible-role-firewalld/workflows/Molecule%20Test/badge.svg)

Manage firewalld for CentOS 7, Rocky Linux 8, Rocky Linux 9, Ubuntu 20.04, and Ubuntu 22.04.

Requirements
------------

None

Role Variables
--------------

See defaults/main.yml

Dependencies
------------

None

Example Playbook
----------------

    - name: Converge
      hosts: all
      become: true
    
      vars:
        - firewalld:
            - zone: dmz
              service: http
              permanent: true
              state: enabled
            - zone: dmz
              service: https
              permanent: true
              state: enabled
    
      roles:
        - role: ansible-role-firewalld

License
-------

BSD

Author Information
------------------

Kevin Coakley (https://github.com/kevincoakley)
