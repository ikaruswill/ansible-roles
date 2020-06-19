OS
=========

Perform standard steps for all operating systems

Requirements
------------

None

Role Variables
--------------

| Variable                | Description                                                               | Default |
|-------------------------|---------------------------------------------------------------------------|---------|
| os_passwordless_sudoers | List of linux users on target host to allow `sudo` usage without password | []      |

Dependencies
------------

None

Example Playbook
----------------
```yaml
- hosts: all
  roles:
  - os
```

License
-------

BSD

Author Information
------------------
ikaruswill
