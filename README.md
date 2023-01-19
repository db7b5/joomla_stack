# joomla_stack
Creating a Joomla stack with docker

Joomla is a popular content management system (CMS) that allows you to easily create and manage websites. One of the great things about Joomla is that it can be easily deployed using Docker, making it a great option for developers and web administrators who want to quickly set up a Joomla site. In this blog post, we will show you how to use Docker Compose to create a Joomla stack that includes MariaDB as the database, Joomla as the web server, and phpMyAdmin as the database management tool. This is particularly useful if you are experimenting with Joomla in your homelab.

Docker Compose is a tool that allows you to define and run multi-container Docker applications. With Compose, you can easily configure and start all the services that make up a Joomla stack using a single command. This makes it perfect for experimenting with Joomla in your homelab, as you can easily spin up a test environment without having to worry about configuring the various components of a Joomla stack manually.

The first step in creating a Joomla stack with Docker Compose is to create a docker-compose.yml file. This file describes the services that make up the stack and how they are configured. Here you will find an example of a docker-compose.yml file for a Joomla stack

This file creates containers for Joomla, MySql and phpmyadmin.

The phpMyAdmin service uses the phpmyadmin/phpmyadmin image, it is also linked to the MariaDB service and is configured with environment variables such as PMA_HOST, PMA_PORT and MYSQL_ROOT_PASSWORD, it maps the container’s port 80 to the host’s port 8080.

With the docker-compose.yml file in place, you can start the Joomla stack by running the following command in the same directory as the file:

docker-compose up

This command will start all the services defined in the docker-compose.yml file, including the MariaDB service, the Joomla service, and the phpMyAdmin service. Once the services are running, you can access the Joomla installation at http://localhost or http://host-ip
