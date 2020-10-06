# Ansible playbook for install LEMP with Drupal or Wordpress

### List of roles
- ansible-lemp-php
- ansible-lemp-mariadbase
- ansible-lemp-drupal
- ansible-lemp-wordpress
- ansible-lemp-nginx


Ansible LEMP + Drupal | WordPress
==================
- nginx: latest
- php: 7.2 | 7.3 (tested)
- mariadb: latest

Supports platforms:
-------------------
- Ubuntu (18.04 | 20.04) 

Variables
--------------
Package variables are located in group_vars/all.yml

## Usage example

### Run Playbook 
----------------------------------------------------------
*default setup: nginx: latest, php: 7.2, mariadb: latest, ssl generate*

For Drupal install: 
```bash
ansible-playbook drupal.yml
```
For WordPress install:
```bash
ansible-playbook drupal.yml
``` 

Using another php version (example):
----------------------------------------------------------
```bash
ansible-playbook wordpress.yml -e php_ver=7.3
```

Default variables witch can be changed:
```
pool_name: 
php_ver: [7.2, 7.3]
lets_gen: [true | false]
domain: 
lets_email: 
mysql_root_pass: 
site_dir: 
```