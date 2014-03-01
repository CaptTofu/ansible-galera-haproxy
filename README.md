Role Name
========

ansible-galera-haproxy -- build an haproxy node that proxies a galera cluster

Requirements
------------

A 3-node setup using ansible-galera role (see ansible-galera role README)

Role Variables
--------------

None

Dependencies
------------

None

License
-------

Apache 2.0

Author Information
------------------

Patrick "CaptTofu" Galbraith <patg@hp.com> <patg@patg.net>

How do I use this?
------------------

1. Setup of ansible-galera-haproxy per README 

2. ansible-galaxy install --force --roles-path=/where/ever/you/want/your/roles CaptTofu.ansible-galera-haproxy

3. Add three galera hosts to your ansible hosts file that already has the galera nodes (you'll need them in there.

    [galera_cluster]
    host1
    host2
    host3

    [haproxy]
    host4

4. Use it in your playbook:


    - hosts: 
      - haproxy 
    roles:
      - CaptTofu.ansible-galera-haproxy

3. Run your playbook (this is for Docker)

    ansible-playbook -i hosts -u root haproxy.yml

