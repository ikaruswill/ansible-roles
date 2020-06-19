Base
=========

Perform standard steps for all operating systems

Requirements
------------

None

Role Variables
--------------

| Variable            | Description                                           | Default     |
|---------------------|-------------------------------------------------------|-------------|
| base_default_locale | The default locale to be set at `/etc/default/locale` | en_US.UTF-8 |
| base_apt_packages   | Apt-packages to be installed                          | Essentials  |

Dependencies
------------

None

Example Playbook
----------------
```yaml
- hosts: all
  roles:
  - base
```

License
-------

BSD

Author Information
------------------
ikaruswill
