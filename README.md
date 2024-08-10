OpenSSH
=======

An Ansible role to configure the OpenSSH server and client.

Requirements
------------

- Supported version of Ansible: 2.12 and highter.
- `pywinrm` is a python library for connection Ansible to Windows hosts via [WinRM](https://docs.ansible.com/ansible/latest/user_guide/windows_winrm.html).
- Supported platforms:
  - Amazon Linux
    - 2
    - 2023
  - Debian
    - 10
    - 11
    - 12
  - Fedora
    - 39
    - 40
  - RHEL
    - 7
    - 8
    - 9
  - Ubuntu
    - 18.04
    - 20.04
    - 22.04
  - Windows
    - 2019

Role Variables
--------------

All variables that can be overridden are stored in the [defaults/main.yml](https://github.com/antmelekhin/ansible-role-openssh/blob/main/defaults/main.yml) file.
Please refer to the [meta/argument_specs.yml](https://github.com/antmelekhin/ansible-role-openssh/blob/main/meta/argument_specs.yml) file for a description of the available variables.
Similarly, descriptions and defaults for preset variables can be found in the [vars/main.yml](https://github.com/antmelekhin/ansible-role-openssh/blob/main/vars/main.yml) file.

Dependencies
------------

None.

Example Playbook
----------------

Configure OpenSSH server and enable single sign-on.

```yaml
---
- name: 'Setup OpenSSH'
  hosts: all

  roles:
    - role: 'antmelekhin.openssh'
      openssh_sshd_password_authentication: true
      openssh_sshd_gssapi_authentication: true
```

Configure OpenSSH server and enable single sign-on for server_admins group.

```yaml
---
- name: 'Setup OpenSSH'
  hosts: all

  roles:
    - role: 'antmelekhin.openssh'
      openssh_sshd_match:
        - type: 'Group'
          name: 'server_admins'
          config:
            PasswordAuthentication: 'yes'
            GSSAPIAuthentication: 'yes'
```

License
-------

MIT

Author Information
------------------

Melekhin Anton.
