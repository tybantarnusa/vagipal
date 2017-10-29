# Vagipal

Vagipal is an experimental Vagrant based development environment for Drupal.

## Inside Vagipal
- Ubuntu 16.04 (ubuntu/xenial64)
- Apache 2
- PHP 7
- MySQL
- PhpMyAdmin
- Git
- Composer
- Drupal 7.56
- Drush (CLI for Drupal)

## How to Use
1. Install VirtualBox: https://www.virtualbox.org/
2. Install Vagrant: http://www.vagrantup.com/
3. Download Ubuntu 16.04 64-bit box for Vagrant
```bash
$ vagrant box add ubuntu/xenial64
```
4. Download Vagipal
if you use git:
```bash
$ git clone https://github.com/tybantarnusa/vagipal.git
```
or if you don't have git installed:
```bash
$ wget https://github.com/tybantarnusa/vagipal/archive/master.zip
$ unzip master.zip
$ mv ./vagipal-master ./vagipal
```

5. Go to Vagipal directory
```bash
$ cd vagipal
```

6. __OPTIONAL__: Install the vagrant-hostsupdater plugin
```bash
$ vagrant plugin install vagrant-hostsupdater
```
Use this if you want your drupal site to be accessed via named domain such as `http://vagipal.dev/`. You can change the host name by editing the file `provisioning/default.yml`.

__WARNING!__ Windows does not allow to change hosts files. Add `vagipal.dev 118.97.103.105` by yourself.

7. Start the Vagrant environment
```bash
$ vagrant up
```
This will take quite a long time. So, be patient. Please understand.

8. Open your Drupal site in browser

by accessing `118.97.103.105`, or `vagipal.dev` if you use hostsupdater and didn't change the hostname configuration in `provisioning/default.yml`

## Default Configurations
### Drupal
- Username: `admin`
- Password: `admin`

### MySQL
- Host: `127.0.0.1`
- Username: `root`
- Password: `password`
- Port: `3306`

## CLI
You can access your Vagrant environment using:
```bash
$ vagrant ssh
```

Vagipal uses Drush as command-line interface for Drupal. See more about Drush here: http://www.drush.org/.

## How to Contribute
1. Clone this repository
```bash
$ git clone https://github.com/tybantarnusa/vagipal.git
```
2. Start coding!
3. Send pull request to this repository

## Epilogue
This project is maintained by __Thoyib Antarnusa__ initially for mid-term project in Open-Source Software Development class of Faculty of Computer Science, Universitas Indonesia.
