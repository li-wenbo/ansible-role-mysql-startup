mysql-startup
=========

This role is used for install a mysql Server using binary file downloaded from mysql.com

Requirements
------------

1. pip

Role Variables
--------------

1. you should select a mysql_server_id for every mysql server, and they are different. put it in the inventory.

        [dbs]
        10.0.10.11 mysql_server_id=1
        10.0.10.12 mysql_server_id=2

2. default mysql_server_port is 3306
3. must change mysql_root_password in default/main.yml

Dependencies
------------

[]

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: mysql-startup, mysql_server_port: 3306, mysql_root_password: "passed from ansible-playbook -e is better" }

License
-------

BSD

Author Information
------------------

liwb/li.wenbo2@qq.com
