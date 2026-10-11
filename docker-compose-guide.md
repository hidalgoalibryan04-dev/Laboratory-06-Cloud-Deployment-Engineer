# Docker Compose Guide

## Introduction

Docker Compose is a tool that allows me to define and manage multiple containers using a YAML configuration file. In this laboratory, I used it to deploy Nextcloud and MariaDB together instead of starting each container manually.

## The `services:` Block

The `services:` block defines the containers that make up the application. In my configuration, I created two services named `database` and `app`.

* **database:** Uses the MariaDB 10.6 image and defines the database name, username, and passwords.
* **app:** Uses the Nextcloud image, exposes port 8080 on the host, and contains the settings needed to connect to MariaDB.

These settings tell Docker Compose what images to use and how the services should be configured.

## How Nextcloud Finds the Database

The environment variable `MYSQL_HOST=database` tells Nextcloud where to find the database service. The name `database` is the service name defined in the Compose file. Docker Compose creates a network for the services, allowing the Nextcloud container to reach MariaDB using that name.

The database credentials and database name must also match between the application and database configurations so that Nextcloud can connect successfully.

## Docker Run vs. Docker Compose

The `docker run` command starts an individual container and allows me to specify its settings through command-line options. If I need several connected containers, I may have to configure their networks, ports, and environment variables separately.

On the other hand, `docker-compose up -d` reads the configuration from the Compose file and starts the defined services together in the background. I find this approach easier to repeat because I can keep the deployment settings in one file.

## Commands Used

### 1. Create the project directory

```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
```

### 2. Create the Compose file

```bash
nano docker-compose.yml
```

### 3. Deploy the services

```bash
docker-compose up -d
```

The `-d` option runs the containers in the background.

### 4. Check the container status

```bash
docker-compose ps
```

This command displays the status of the services managed by the Compose project.

### 5. Stop and remove the containers

```bash
docker-compose down
```

This command stops and removes the project's containers and its default network. It does not automatically remove named volumes unless the appropriate volume-removal option is used.

## Infrastructure as Code (IaC)

Infrastructure as Code means defining infrastructure settings in configuration files instead of relying only on manual commands. In this activity, the Compose file serves as a blueprint for the Nextcloud deployment. I can reuse the file to create the same basic environment again, making the process more consistent and easier to document.

## Conclusion

I learned that Docker Compose is useful for applications that need multiple connected services. It reduces repetitive commands and helps me organize deployment settings in one place.
