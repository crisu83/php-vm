# PHP-VM

A scalable project template for any PHP application.

This stack consists of the following building blocks:

- [VirtualBox](https://www.virtualbox.org)
- [Vagrant](https://www.vagrantup.com)
- [Ansible](http://www.ansible.com)
- [Nginx](http://www.nginx.com)
- [MariaDB](https://mariadb.com)
- [PHP-FPM](http://php-fpm.org)
- [Composer](https://getcomposer.org)

## Installation

Follow these steps to setup your own PHP-VM:

- Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads), [Vagrant](https://www.vagrantup.com/downloads.html) and [Ansible](http://docs.ansible.com/intro_installation.html)
- Clone the project and run ```vagrant up``` in the project folder to create your virtual machine
- Once the machine is up you should be able to access it through your browser by navigating to http://localhost:1337

Now you can run ```vagrant ssh``` to SSH into the virtual machine and use Composer to install anything you like.
