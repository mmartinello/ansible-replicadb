Ansible ReplicaDB
=================

This role install [ReplicaDB](https://osalvador.github.io/ReplicaDB/) on a Linux system.

Requirements
------------

None.

Role Variables
--------------

Variables are listed into the `defaults/main.yml` file, with description and
default value:

```
# ReplicaDB version to be installed
replicadb_version: latest

# ReplicaDB installation target path
replicadb_path: /opt/replicadb

# Reinstall ReplicaDB if already installed
replicadb_reinstall: false

# ReplicaDB installed: if true do not (re)install
replicadb_installed: false
```

Dependencies
------------

ReplicaDB requires Java.
For this reason, this role requires the `geerlingguy.java` Ansible role to
install Java:

```
ansible-galaxy install geerlingguy.java
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
    - hosts: servers
      roles:
         - role: mmartinello.replicadb
```

License
-------

MIT / BSD

Author Information
------------------

Mattia Martinello: *mattia (at) mattiamartinello.com*
