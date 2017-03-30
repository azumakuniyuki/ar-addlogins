Ansible Role: addlogins
================================================================================
Add groups and users at UNIX like operating systems

- Add `wheel` group
- Add login users and groups defined in `addlogins.unixusers` variable

Requirements
--------------------------------------------------------------------------------
No requirements.

Role Variables
--------------------------------------------------------------------------------
The following variables are defined in `defaults/main.yml` file for being added.

```yaml
addlogins:
  enabled: false
  belongsto:
    - group: wheel
      users: ['admin']
  unixusers:
    - username: admin
      password: $1$HakataNo$9.s0dLxBeUTgTarKe3uU//
      shell: /bin/sh
      group: admin
      home: /home/admin
      uid: 1001
      gid: 1001
```

Dependencies
--------------------------------------------------------------------------------
None.

Example Playbook
--------------------------------------------------------------------------------
```yaml
- hosts: servers
  roles:
     - { role: azumakuniyuki.addlogins, addlogins.enabled: true }
```

License
--------------------------------------------------------------------------------
BSD

Author Information
--------------------------------------------------------------------------------
[azumakuniyuki](http://nyaan.jp/)

