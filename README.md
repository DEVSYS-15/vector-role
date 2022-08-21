DEVSYS-15.Vector
=========

Downdload and install Vector

Requirements
------------
```
  - src: git@github.com:AlexeySetevoi/ansible-clickhouse.git
    scm: git
    version: "1.11.0"
    name: my_clickhouse 
```

Role Variables
--------------
```
vector_version: "1"
vector_release: "0.22.2"

clickhouse_http_port: "8123"

clickhouse:
  hosts:
    clickhouse-01:
      ansible_host: 172.17.2.62

vector_url: "https://packages.timber.io/vector/{{ vector_release }}/vector-{{ vector_release }}-{{ vector_version }}.x86_64.rpm"
```
Dependencies
------------

NO Dependencies

Example Playbook
----------------

```
- name: Install Vector
  hosts: 
   - vector
  roles:
    - DEVSYS-15.Vector
  tags: 
    - "Install Vector"
```
License
-------

BSD

Author Information
------------------
DEVSYS-15
