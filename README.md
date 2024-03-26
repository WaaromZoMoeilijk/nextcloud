Nextcloud (Latest)
=========

Ansible Playbook to install

* Nextcloud (Latest) - <https://nextcloud.com/>
* nginx (Latest) - <https://nginx.org/>
* PHP 8.2 - <http://www.php.net/>
* PostgreSQL (Latest) <https://www.postgresql.org/>
* redis - <https://redis.io/>
* restic backup - <https://restic.readthedocs.io>
* Onlyoffice <https://www.onlyoffice.com>

Most of the settings are recommentations from C. Rieger

Visit his page for all details: <https://www.c-rieger.de/>

Requirements
------------

Ubuntu 22.04

Install
-------

```bash
# prepare your os and install ansible
curl -s https://raw.githubusercontent.com/ReinerNippes/nextcloud/master/prepare_system.sh | /bin/bash

# clone this repo
git clone https://github.com/ReinerNippes/nextcloud

# change to nextcloud directory
cd nextcloud

# edit variables
nano inventory

# run the playbook
./nextcloud.yml -e 'ansible_python_interpreter=/usr/bin/python3'
```

> **WARNING**: Remember to update the inventory file if you want to run the playbook later again. E.g. to update the system. If you don't the defaults in the inventory file will be apply during the second run.

Login to your nextcloud web site <https://nc.example.org>

Users and passwords have been set according to the entries in the inventory if defined there. Otherwise the admin password will be displayed at the end of playbook. Additional you can find them in the credential_store = /etc/nextcloud

Role Variables
--------------

All variables are defined in inventory file.

-----------------------

If you find this Playbook helpful and want to donate something. Please go to this web page donate for children in need. 

https://wir-fuer-kinder-in-not.org/ and click on "Spenden" (Donate)
