# ansible-role-hosts

Simple role to make all hosts within the inventory (group) known to each other. Since it uses the group 'all', all hosts of the inventory will be added.  
This can be useful if you dont have a DNS in place and want to use Hostnames.

Entries for all hosts are created in /etc/hosts on all hosts.  
This is done using hostvars.ansible_default_ipv4.address and hostvars.ansible_fqdn. So the currently hostname of the machine will be used!

## Example Usage

```
---
- hosts: all
  become: true
  roles:
    - tbauriedel.hosts
```
