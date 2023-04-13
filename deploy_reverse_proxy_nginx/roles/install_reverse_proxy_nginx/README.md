Install Reverse Proxy Nginx
=========

Данная роль создает и настраивает reverse proxy на сервисы с помощью субдоменов на базе Nginx.

Requirements
------------

Использование ОС Ubuntu/Debian, настроенный домен на узел и созданные под субдомены сертификаты.

Role Variables
--------------

domain       - используемый домен, который настроен на узел, на котором разворворачиваем обратный прокси Nginx.
list_service - список сервисов, на которые будет перенаправлять обратный прокси Nginx.

Dependencies
------------

create_cert_for_subdomain - данная роль из списка сервисов из переменной list_service создается сертификат {{ service }}.{{ domain }};

Example Playbook
----------------

- name: Install Reverse Proxy Nginx
  hosts: all
  become: yes
  roles:
    - install_reverse_proxy_nginx

License
-------

BSD

Author Information
------------------

Author: Nikira Grigorev
GitHub: https://github.com/modon1999
