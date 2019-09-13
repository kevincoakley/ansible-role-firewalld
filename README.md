ansible-role-firewalld
======================

[![Build Status](https://travis-ci.org/kevincoakley/ansible-role-firewalld.svg?branch=master)](https://travis-ci.org/kevincoakley/ansible-role-firewalld)

Manage firewalld for CentOS 7

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
