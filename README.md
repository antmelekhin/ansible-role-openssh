OpenSSH
=======

Ansible роль для настройки OpenSSH сервера.

Требования
----------

- Поддерживаемая версия Ansible: 2.9 и выше.
- `pywinrm` для подключения [Ansible через WinRM](https://docs.ansible.com/ansible/latest/user_guide/windows_winrm.html) (для Windows).
- Список поддерживаемых платформ описан в файле метаданных роли.

Используемые переменные
-----------------------

Переменные описаны в `defaults\main.yml`.

Зависимости
-----------

Отсутствуют.

Пример использования
--------------------

- Настраиваем OpenSSH сервер, включаем автоматическую аутентификацию (single sign-on).

  ```yaml
  ---
  - name: 'Setup OpenSSH'
    hosts: all

    roles:
      - role: 'antmelekhin.openssh'
        openssh_sshd_password_authentication: true
        openssh_sshd_gssapi_authentication: true
  ```

- Настраиваем OpenSSH сервер, включаем автоматическую аутентификацию (single sign-on) для группы пользователей.

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

Лицензия
--------

MIT

Информация об авторе
--------------------

Мелехин Антон.
