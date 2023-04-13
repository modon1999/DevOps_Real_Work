Create Cert for Subdomain
=========

Данная роль создает сертификаты для сервисов.

Requirements
------------

Использование ОС Ubuntu/Debian, и настроенный домен на узел.

Role Variables
--------------

email        - email для создания сертификатов Let's Encrypt.
domain       - используемый домен, который настроен на узел, на котором разворворачиваем обратный прокси Nginx.
list_service - список сервисов, на которые будет перенаправлять обратный прокси Nginx.

Dependencies
------------

Зависимостей данная роль не имеет

Example Playbook
----------------

- name: Create Cert for Subdomain
  hosts: all
  become: yes
  roles:
    - create_cert_for_subdomain

License
-------

BSD

Author Information
------------------

Author: Nikira Grigorev
GitHub: https://github.com/modon1999
