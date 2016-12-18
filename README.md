ansible-role-mas
================

A brief description of the role goes here.

Requirements
------------

There are issues downloading apps from the Mac App Store when running with Ansible over SSH.
Therefore, this role requires `ansible_connection=local`.

Role Variables
--------------

    mas_email: the Mac App Store email
    mas_password: the Mac App Store password

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

[Roman Khmelichek](http://romankh.me/)
