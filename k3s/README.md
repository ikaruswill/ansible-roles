Base
=========

Install k3s on a cluster, with a single master node.

Requirements
------------

None

Role Variables
--------------

| Variable            | Description                                                              | Default                                      |
|---------------------|--------------------------------------------------------------------------|----------------------------------------------|
| k3s_master.hostname | Hostname of the desired master node (Must be same as inventory hostname) | Required                                     |
| k3s_master.ip       | IP address of the desired master node                                    | Required                                     |
| k3s_master.flags    | Flags to pass to the installation script on the master node              | [--no-deploy servicelb, --no-deploy traefik] |
| k3s_version         | Version of k3s to install, defaults to the latest release if empty       | ''                                           |

Dependencies
------------

None

Example Playbook
----------------
```yaml
- hosts: all
  roles:
  - k3s
```

License
-------

BSD

Author Information
------------------
ikaruswill
