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

### Local VM

- Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads), [Vagrant](https://www.vagrantup.com/downloads.html) and [Ansible](http://docs.ansible.com/intro_installation.html)
- Install the Vagrant-Env plugin by running ```vagrant plugin install vagrant-env```
- Clone the project and run ```vagrant up``` in the project folder to create your virtual machine
- Once the machine is up you should be able to access it through your browser by navigating to http://localhost:1337

### Digital Ocean Droplet

- Install [Vagrant](https://www.vagrantup.com/downloads.html) and [Ansible](http://docs.ansible.com/intro_installation.html)
- Install the Vagrant-Env plugin by running ```vagrant plugin install vagrant-env```
- Create your account on [Digital Ocean](https://www.digitalocean.com/), confirm your email address and log in
- Generate an API token in the **Apps & API** section of the management panel
- Clone the project and create a ```.env``` file in the project root with your environmental variables
- Run ```vagrant up --provider=digital_ocean``` in the project folder to create your droplet

Now you can run ```vagrant ssh``` to SSH into the virtual machine and use Composer to install anything you like.
