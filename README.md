OpenSSH
=======

An Ansible role for configure OpenSSH server and client.

Requirements
------------

- Supported version of Ansible: 2.12 and highter.
- `pywinrm` is a python library for connection Ansible to Windows hosts via [WinRM](https://docs.ansible.com/ansible/latest/user_guide/windows_winrm.html).
- Supported platforms:
  - Debian
    - 10
    - 11
    - 12
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

- `openssh_sshd_port` Specifies the port number that sshd listens on. (default: `22`).
- `openssh_sshd_address_family` Specifies which address family should be used by sshd.

  Valid values:
  - `any` (the default)
  - `inet` (use IPv4 only)
  - `inet6` (use IPv6 only)

- `openssh_sshd_listen_addresses` Specifies the local addresses sshd should listen on.
- `openssh_sshd_host_keys_dir` and `openssh_sshd_host_keys` Specifies a file containing a private host key used by sshd.
- `openssh_sshd_syslog_facility` Gives the facility code that is used when logging messages from sshd (default: `AUTH`).
- `openssh_sshd_log_level` Gives the verbosity level that is used when logging messages from sshd (default: `INFO`).
- `openssh_sshd_login_grace_time` The server disconnects after this time if the user has not successfully logged in. (default: `1m`).
- `openssh_sshd_max_auth_tries` Specifies the maximum number of authentication attempts permitted per connection. (default: `4`).
- `openssh_sshd_max_sessions` Specifies the maximum number of open shell (default: `10`).
- `openssh_sshd_max_startups` Specifies the maximum number of concurrent unauthenticated connections to sshd (default: `10:30:60`).
- `openssh_sshd_authorized_keys_file` Specifies the file that contains the public keys used for user authentication (default: `.ssh/authorized_keys`).
- `openssh_sshd_password_authentication` Specifies whether password authentication is allowed (default: `false`).
- `openssh_sshd_kerberos_authentication` Specifies whether the password provided by the user for `openssh_sshd_password_authentication` will be validated through the Kerberos KDC. Not applicable in Windows (default: `false`).
- `openssh_sshd_kerberos_ticket_cleanup` Specifies whether to automatically destroy the user's ticket cache file on logout. Not applicable in Windows (default: `true`).
- `openssh_sshd_gssapi_authentication` Specifies whether user authentication based on GSSAPI is allowed. Not applicable in Windows (default: `false`).
- `openssh_sshd_gssapi_cleanup_credentials` Specifies whether to automatically destroy the user's credentials cache on logout. Not applicable in Windows (default: `true`).
- `openssh_sshd_strict_modes` Specifies whether sshd should check file modes and ownership of the user's files and home directory before accepting login. Not applicable in Windows (default: `true`).
- `openssh_sshd_permit_root_login` Specifies whether root can log in using sshd (default: `false`).
- `openssh_sshd_tcp_keep_alive` Specifies whether the system should send TCP keepalive messages to the other side (default: `false`).
- `openssh_sshd_client_alive_interval` Sets a timeout interval in seconds after which if no data has been received from the client (default: `0`).
- `openssh_sshd_client_alive_count_max` Sets the number of client alive messages which may be sent without sshd receiving any messages back from the client (default: `3`).
- `openssh_sshd_x11_forwarding` Specifies whether X11 forwarding is permitted. Not applicable in Windows (default: `false`).
- Controlling which users and groups can connect to the server is done using the `openssh_sshd_allow_groups`, `openssh_sshd_allow_users`, `openssh_sshd_deny_groups`, and `openssh_sshd_deny_users` lists (default: `[]`).
- `openssh_sshd_use_dns` Specifies whether sshd should look up the remote host name, and to check that the resolved host name for the remote IP address maps back to the very same IP address. (default: `false`).
- `openssh_sshd_subsystems` Configures an external subsystem (e.g. file transfer daemon).

  The default value:
  - `sftp: '/usr/libexec/openssh/sftp-server'` (for RedHat)
  - `sftp: '/usr/lib/openssh/sftp-server'` (for Debian)
  - `sftp: 'C:\Windows\System32\OpenSSH\sftp-server.exe'` (for Windows)

- `openssh_sshd_match` A conditional block. The arguments to Match are one or more criteria-pattern pairs or the single token All which matches all criteria. The available criteria are User, Group, Host, LocalAddress, LocalPort, RDomain and Address (See example).

Dependencies
------------

None.

Example Playbook
----------------

- Configure OpenSSH server and enable single sign-on.

  ```yaml
  ---
  - name: 'Setup OpenSSH'
    hosts: all

    roles:
      - role: 'antmelekhin.openssh'
        openssh_sshd_password_authentication: true
        openssh_sshd_gssapi_authentication: true
  ```

- Configure OpenSSH server and enable single sign-on for server_admins group.

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
