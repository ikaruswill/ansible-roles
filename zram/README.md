ZRAM
=========

Install and configure `zram-config`. Optionally upgrade zram-config if a newer version is available.

Requirements
------------

None

Role Variables
--------------

| Variable                        | Description                                                                                                                                       | Default                         |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------- |
| zram_upgrade                    | Should zram-swap be upgraded if a newer version is available?                                                                                     | false                           |
| zram_swap_default_swap_priority | Default swap priority if none specified                                                                                                           | 75                              |
| zram_swap_default_page_cluster  | Default page cluster if none specified                                                                                                            | 0                               |
| zram_swap_default_swappiness    | Default swappiness if none specified                                                                                                              | 150                             |
| zram_log_default_target_dir     | Default target_dir if none specified                                                                                                              | /var/log                        |
| zram_log_default_bind_dir       | Default bind_dir if none specified                                                                                                                | /opt/zram/log.bind              |
| zram_log_default_oldlog_dir     | Default oldlog_dir if none specified                                                                                                              | /opt/zram/oldlog                |
| <zram_device>.alg               | Compression algorithm to use                                                                                                                      |                                 |
| <zram_device>.mem_limit         | Maximum physical memory that the swap may occupy                                                                                                  |                                 |
| <zram_device>.disk_size         | Maximum size to advertise after factoring in compression                                                                                          |                                 |
| zram_swap                       | Swap device configuration attributes, if mapping is omitted, no swap device will be created.                                                      |                                 |
| zram_swap.swap_priority         | Priority of the zram swap device over other swap devices                                                                                          | zram_swap_default_swap_priority |
| zram_swap.page_cluster          | Number of memory pages up to which consecutive pages are read in from swap. Set to 0 for zram for low latency. Values are taken as powers of 2.   | zram_swap_default_page_cluster  |
| zram_swap.swappiness            | How often should the swap device be utilized? For zram, value should be > 100. Can be set to 200 for improved performance in high memory pressure | zram_swap_default_swappiness    |
| zram_log                        | zram log device configuration attributes, if mapping is omitted, no zram log device will be created.                                              |                                 |
| zram_log.target_dir             | Target directory with which to mount the zram device                                                                                              | zram_log_default_target_dir     |
| zram_log.bind_dir               | Path where the original directory will be mounted for persistence                                                                                 | zram_log_default_bind_dir       |
| zram_log.oldlog_dir             | Path where the rotated logs will be stored                                                                                                        | zram_log_default_oldlog_dir     |

Dependencies
------------

None

Example Playbook
----------------
```yaml
- hosts: all
  roles:
  - zram
  vars:
    zram_log:
      alg: lzo-rle
      mem_limit: 64M
      disk_size: 192M
    zram_swap:
      alg: lzo-rle
      mem_limit: 512M
      disk_size: 1024M
```

License
-------

BSD

Author Information
------------------
ikaruswill
