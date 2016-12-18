ansible-role-mas
================

[![Build Status](https://travis-ci.org/rkhmelichek/ansible-role-mas.svg?branch=master)](https://travis-ci.org/rkhmelichek/ansible-role-mas)

Installs apps from the Mac App Store.

Requirements
------------

There are issues downloading apps from the Mac App Store when running with Ansible over SSH.
Therefore, this role requires `ansible_connection=local`.
The `mas-cli` tool must be installed prior to running this role.

Role Variables
--------------

    mas_email: the Mac App Store email
    mas_password: the Mac App Store password
    mas_apps: a list of Mac App Store apps to install

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: localhost
      vars:
        homebrew_prefix: /usr/local
      vars_prompt:
        - name: "mas_email"
          prompt: "Enter Mac App Store email"
          private: no
        - name: "mas_password"
          prompt: "Enter Mac App Store password"
          private: yes
      roles:
        - rkhmelichek.mas
          mas_apps:
            - { name: 1Password, id: 443987910 }

License
-------

BSD

Author Information
------------------

[Roman Khmelichek](http://romankh.me/)
