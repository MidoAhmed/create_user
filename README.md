[![Build Status](https://travis-ci.org/MidoAhmed/create_user.svg?branch=master)](https://travis-ci.org/MidoAhmed/create_user)

create_user
=========

Create a user and upload an ssh public key for remote authentification

Requirements
------------

- No specific required Ansible.

- Needs a default ssh public key or a specific key needs to be called out in a variable

Role Variables
--------------


Define the user you would to create.
>user_name: default

Define the state present or absent
>user_state: present

Define the path to ssh public key
>ssh_key: ~/.ssh/id_rsa.pub

Dependencies
------------

None

Example Playbook
----------------

```
---
- hosts: all
  tasks:
     - include_role:
         name: create_user
       vars:
         user_name: robert
         ssh_key: ./ssh/id_rsa.pub
```

License
-------

MIT

Author Information
------------------

- test@gmail.com
