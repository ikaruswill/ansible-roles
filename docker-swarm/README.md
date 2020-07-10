Base
=========

Install Docker if it does not exist, initialize a swarm, and join all nodes into the swarm.

Requirements
------------

None

Role Variables
--------------

| Variable                      | Description                                                               | Default  |
|-------------------------------|---------------------------------------------------------------------------|----------|
| docker_swarm_manager.hostname | Hostname of the desired manager node (Must be same as inventory hostname) | Required |
| docker_swarm_manager.ip       | IP address of the desired manager node                                    | Required |

Dependencies
------------

None

Example Playbook
----------------
```yaml
- hosts: all
  roles:
  - docker-swarm
```

License
-------

BSD

Author Information
------------------
ikaruswill
