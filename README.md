# ccnas-ansible
## Lab 1

First lab task can be done by running `lab1.yaml`. Alternatively it can be done by running the following commnands:

**Get IP Address:**
```
ansible -i hosts routers -m ios_command -a "commands='sh ip int br'" -e ansible_connection=network_cli -e ansible_network_os=ios -u admin --ask-pass --become
```
**Get IP Routing Table:**
```
ansible -i hosts routers -m ios_command -a "commands='sh ip route'" -e ansible_connection=network_cli -e ansible_network_os=ios -u admin --ask-pass --become
```
**Get ARP Table:**
```
ansible -i hosts routers -m ios_command -a "commands='sh arp'" -e ansible_connection=network_cli -e ansible_network_os=ios -u admin --ask-pass --become
```