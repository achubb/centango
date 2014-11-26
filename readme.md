# Centango Vagrant Box - CentOS/Django/Postgres Development Environment

Centango Vagrant Box is a lightweight [vagrant](http://vagrantup.com) box running CentOS 6.5 for Django development. The box has a simple initiated Django project hooked up to a PostgreSQL database. The primary purpose of this box is to mimic a CentOS server environment.

## What's Included

The basic componenets for running a small Django site, including:

* CentOS 6.5 [here](https://vagrantcloud.com/chef/boxes/centos-6.5)
* Python 2.6.6
* PostgreSQL 8.4.20
* python-pip
* django 1.6
* virtualenvwrapper
* psycopg2


## Instructions

In the vagrantfile the vagrant box is configured with a network ip of *192.168.234.111* and a hostname of *centango.dev*. You can change these values to suit your own needs. However you will need to add an entry into your hosts file like so:

	192.168.234.111 centango.dev

Ensure that you have Vagrant installed and set up on your machine. Follow the instructions [here](https://docs.vagrantup.com/v2/installation/index.html)

Clone the repo to the desired location and run:

	vagrant up

Then, once the vagrant box is initialised run:

	vagrant ssh

Navigate to the synced folder (cd ../../vagrant). This is where the demo Django project has been set up. From here you can go into the project directory.

	cd mysite

I have set up a virtualenv simply called *project*. To activate this virtual environment run:

	workon project

Then, to run the local server, simply run:

	djrun

This will invoke the local server. If you set up your hosts file in the above steps, then you should be able to go to http://centango.dev:8000 and you should see the running Django site.  

## Administration

To get straight into the Django admin. You can go to http://centango.dev:8000/admin and use the following creadentials.

u: *admin*
p: *nimda*
