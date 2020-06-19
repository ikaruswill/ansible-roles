Rpi
=========

Perform standard steps for headless Rpi installations

Requirements
------------

Raspbian or derivative operating systems

Role Variables
--------------

| Variable                | Description                                                     | Default  |
|-------------------------|-----------------------------------------------------------------|----------|
| rpi_tvservice_off_state | The target state to set tvservice to, in order to turn off HDMI | 0x120002 |

Dependencies
------------

None

Example Playbook
----------------
```yaml
- hosts: all
  roles:
  - rpi
```
License
-------

BSD

Author Information
------------------

ikaruswill
