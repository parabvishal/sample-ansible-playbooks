Example Playbook for LAMP stack + HAProxy


- Requires Ansible 1.2 or more
- Expects CentOs 7

In this example we will install and configure simple LAMP stack.
This includes installation of web servers, HAProxy loadbalancer and db servers.

## Configuration Details

configure entire lamp-stack by listing hosts in 'hosts' file as below

[webservers]
web01
web02

[dbservers]
db01

[lbservers]
lb01


After this execute below command to execute the playbook

ansible-playbook -i hosts site.yml


Now verify your configuration by hitting below URL.
http://<IP-OF-LBSERVER>:8080
