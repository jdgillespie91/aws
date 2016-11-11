=======
Vagrant
=======

View boxes with

    vagrant box list

Look for boxes `here <https://atlas.hashicorp.com/boxes/search>`_. Add the desired box with

    vagrant box add ubuntu/trusty32

Create a dev-environment based on a specific box with

    vagrant init ubuntu/trusty32

Start the dev-environment with

    vagrant up

Ssh into the dev-environment with

    vagrant ssh

===============
dev-environment
===============

Update your package repository with

    sudo apt-get update

Try to run mysql with

    mysql

Observe that it is not installed. Install it (using a blank password for root) with

    sudo apt-get install mysql-server

Now run mysql (logging in as root user) with

    mysql -uroot

Complete the installation with the following security commands

    sudo mysql_secure_installation
    sudo mysql_install_db

==========================
Reboot the dev-environment
==========================

Log out of the dev-environment and stop it with

    vagrant halt

Start it with

    vagrant up

Log in with

    vagrant ssh

Observe that everything is as you left it

    mysql -uroot

========================
Save the dev environment
========================

List available snapshots with

    vagrant snapshot list

Snapshot the dev-environment with

    vagrant snapshot push
