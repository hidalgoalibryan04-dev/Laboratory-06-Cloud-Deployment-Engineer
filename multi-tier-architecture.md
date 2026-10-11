# Multi-Tier Architecture

## What Is a Two-Tier Architecture?

A two-tier architecture is an application design that separates an application into two main parts: the web/application tier and the database tier. In this activity, Nextcloud serves as the application, while MariaDB stores the information needed by the system. These two services communicate with each other to make the application work.

## The Web/Application Tier

The web/application tier handles the part of the system that users interact with. In this deployment, Nextcloud provides the web interface where users can access and manage their files. It receives browser requests and communicates with the database when it needs to retrieve or save information.

## The Database Tier

The database tier stores and manages important application data. MariaDB is used to store information such as user accounts, file metadata, and other details needed by Nextcloud. Keeping this information in a database allows the application to retrieve and update records when necessary.

## Why Separate Them?

I think separating the application and database into different containers makes the system easier to manage. Each container has its own responsibility, so I can update or troubleshoot one service without having to rebuild the entire application. It also makes the system more flexible because the services can be configured and scaled separately when needed.

## Architecture Used

* **Application:** Nextcloud
* **Database:** MariaDB 10.6
* **Deployment tool:** Docker Compose
* **Application port:** 8080
* **Database connection:** Docker Compose service name `database`

## Conclusion

From this activity, I learned that a cloud application does not always run as a single service. Different components can work together in separate containers to provide a more organized and manageable system.
