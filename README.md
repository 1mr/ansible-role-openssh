[![Build Status](https://travis-ci.com/1mr/ansible-role-openssh.svg?branch=master)](https://travis-ci.com/1mr/ansible-role-openssh)

Openssh
=======

This role helps to install and configure openssh-server and openssh-client.

Requirements
------------

This role requires ansible 1.4 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

    ssh_port: 2222
    ssh_address:
      - 10.1.5.1
      - 10.1.5.2
    ssh_match_address:
      - name: permit_root_login_yes
        ip:
          - 10.20.1.10
          - 10.20.1.11
        host:
          - app1.example.com
          - app2.example.com
    ssh_trusted_user_ca_keys:
      - "ca"

Variables 'ssh_port' and 'ssh_address' are optional.
Default values for optional variables:

    ssh_port: 22
    ssh_address:
      - 0.0.0.0

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: 1mr.openssh, tags: openssh }

License
-------

MIT

Author Information
------------------

This role was created by Stas Stavnichuk.
