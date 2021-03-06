# Ansible role for RabbitMQ
Ansible role for RabbitMQ 3.7 for CentOS 7

## What's inside?
1. RabbitMQ 3.7
2. Erlang 21.2
3. Custom settings as per `defaults/main.yml`
4. The server is set up to run as system user `rabbitmq`
5. The management UI can be accessed using a Web browser at `http://{node-hostname}:15672/` 
eg. [http://webapp:15672/](). 
6. The default username and password are both set `guest` but works for localhost only.
7. New user `admin` with password `admin` is created and able to access Management tool.

## Interesting dirs and files:
- Logs 
    ```
    /var/log/rabbitmq/
    /var/log/rabbitmq/rabbit@webapp.log - lot of usefull inforamtion
    ```
- Check RabbitMQ's status (as rabbitmq user or root)
    ```
    rabbitmqctl status
    sudo rabbitmqctl status
    ```
How about:
- configuration file ?

## Tested on

## Installation
1. Navigate to Ansible's roles folder
2. Add the repo to git modules
    ```
    git submodule add https://github.com/budnerp/ansible_role_rabbitmq.git ansible_role_rabbitmq
    ```
3. Add the role to Ansible's playbook file
    ```    
    roles:
    [...]
        - ansible_role_rabbitmq
    [...]
    ```

## Other links
- RabbitMQ [http://www.rabbitmq.com/]()
- RabbitMQ Server on GitHub [https://github.com/rabbitmq/rabbitmq-server]()
- Command Line Tools [https://www.rabbitmq.com/cli.html]()

## TO DO
-[ ] add dependencies 
-[ ] check: To have RabbitMQ start as a daemon by default, run the following:
    ```
    chkconfig rabbitmq-server on
    ```

## License
Copyright (c) We Are Interactive under the MIT license.