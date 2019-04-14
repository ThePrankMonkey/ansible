radarr
=========

Installs Radarr.

Requirements
------------

* CentOS
* Internet Connected

Role Variables
--------------

```bash
- radarr_version: 0.2.0.1293 # Version you want to install
- radarr_url: https://github.com/Radarr/Radarr/releases/download/v{{ radarr_version }}/Radarr.develop.{{ radarr_version }}.linux.tar.gz
```

Example Playbook
----------------

```plain
- hosts: radarr
  roles:
  - {name: radarr, become: yes}
```

References
----------

* [Radarr](https://github.com/Radarr/Radarr/)
