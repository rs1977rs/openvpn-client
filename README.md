Role Name
=========

Requirements
------------

Настроенный сервер под CentOS 7, с установленным OpenVPN-сервером.

В папке 'files' созданы папки под каждого клиента.

В них лежат файлы ключей и сертификатов клиента и файл ca.crt.


Role Variables
--------------
```
openvpn_client_name: client1 # имя, под которым будет работать служба
openvpn_server_address: 10.10.10.10 # адрес сервера OpenVPN
openvpn_server_port: 12345 # порт, на котором работает сервер
```
Example Playbook
----------------
```
- hosts: servers
  roles:
    - { role: openvpn-client }
```
