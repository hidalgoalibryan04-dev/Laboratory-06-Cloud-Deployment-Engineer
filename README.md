# Laboratory 06 - Cloud Deployment Engineer

## Mission Overview

In this laboratory activity, I learned how to deploy a private cloud storage system using Docker Compose. I used Nextcloud as the web application and MariaDB as its database. Instead of running each container separately, I used a `docker-compose.yml` file to define the services and deploy them together.

## Objectives

* Understand how a two-tier architecture works.
* Learn how to create a Docker Compose YAML file.
* Deploy Nextcloud and MariaDB using Docker Compose.
* Access the Nextcloud setup page through a web browser.
* Understand the importance of Infrastructure as Code (IaC).
* Practice documenting and organizing my cloud computing projects on GitHub.

## Commands Executed

```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
docker-compose up -d
docker-compose ps
docker-compose down
```

## Skills Learned

Through this activity, I practiced writing YAML configuration files, managing multiple Docker containers, and deploying a web application with a database. I also learned that Docker Compose makes deployment easier because I can define the services in one file and manage them using simple commands.

## Screenshots

The following screenshots will serve as evidence of my deployment process:

* `compose-deployment.png` - Running containers.
* `nextcloud-web.png` - Nextcloud setup page.
* `compose-teardown.png` - Containers stopped and removed.

## Conclusion

This laboratory helped me understand how different application components work together in a cloud environment. I learned that organizing deployment settings in a configuration file can make cloud infrastructure easier to manage and reproduce.
