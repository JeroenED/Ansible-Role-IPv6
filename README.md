Ansible-Role-IPv6
=========

Configures IPv6 networking as documented on [OVH documentation](http://docs.ovh.ca/en/guides-network-ipv6.html)

Requirements
------------

* Ubuntu
* IPv6 capabilities

Role Variables
--------------

ipv6_address: The actual IPv6 address (eg: ::1)
ipv6_netmask: Netmask for IPv6
ipv6_gateway: The gateway (eg: ::1)
ipv6_interface: The interface to confiure (eg. eth0)

All variables are required

Dependencies
------------

(No dependencies)

Example Playbook
----------------

Variables are better placed in `host_vars` as IP-addresses are unique to hosts

```
# playbook-dir/host_vars/localhost.yml

ipv6_address: ::1
ipv6_netmask: 128
ipv6_gateway: ::1
ipv6_interface: eth0
```

```
# playbook-dir/playbook.yml

- hosts: localhost
  roles:
   - { role: jeroened.ipv6 }
```


License
-------

MIT

Author Information
------------------

Contributors:
- Jeroen "JeroenED" De Meerleer <me@jeroened.be> (maintainer)
