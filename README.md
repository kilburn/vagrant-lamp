vagrant-lamp
============

Vagrant configuration for an Ubuntu 12.04 TLS lamp (+phpmyadmin) server

Usage
-----

Open a terminal / command line and just run:

    vagrant up

This will build and run a LAMP server including phpmyadmin. The access credentials are:

- ssh user: vagrant
- password: vagrant
- mysql user: root
- mysql password: vagrant

There are two shared folders to ease development:

- `/var/www` inside the server points to the `web` folder, so that you can edit your files normally and the server picks them up automatically.
- `/vagrant` inside the server points to `./` here. You have access to all files in this repository through that path.

Once the server is started, you can access the website by pointing your browser to [http://localhost:8080/](http://localhost:8080/). You can also access PHPMyAdmin at [http://localhost:8080/phpmyadmin](http://localhost:8080/phpmyadmin) using the mysql credentials above.

*Warning*: the database information is not stored outside the box. You need to dump the
database to the /vagrant folder in the server before destroying it, or you will lose your
databases.
