# Mission 6: The Cloud Deployment Engineer - Reflection

During this laboratory activity, I learned how to use Docker Compose to deploy Nextcloud and MariaDB as two connected services. Before doing this activity, I thought deploying a cloud application mainly involved running a container and opening it in a browser. Now, I understand that applications may need different services working together to function properly.

Writing a `docker-compose.yml` file makes a cloud engineer's job easier because the settings are organized in one place. Instead of typing several commands to configure each container, I can use `docker-compose up -d` to start the services together. I think this is helpful because it saves time and makes the deployment process easier to repeat. It also reduces the chance of forgetting important settings.

I also learned that YAML indentation is important. If I accidentally use a Tab instead of spaces or place a setting at the wrong indentation level, Docker Compose may report an error or interpret the configuration incorrectly. This taught me to check the structure of my file carefully before deploying the application.

Environment variables such as `MYSQL_PASSWORD`, `MYSQL_DATABASE`, and `MYSQL_USER` are used to configure the connection between Nextcloud and MariaDB. I learned that the application and database must use matching credentials and settings for the connection to work. However, I also realized that passwords written directly in a Compose file are suitable only for a basic laboratory exercise and should be handled more securely in real projects.

Deploying a private cloud storage application in a few minutes was interesting because I could see how several containers work together as one system. It helped me appreciate how cloud engineers use automation to make deployment more organized and efficient.

Since Mission 1, my understanding of cloud computing has improved. I now see that cloud computing involves more than storing files online. It also includes managing infrastructure, connecting services, automating deployments, and documenting configurations. This activity encouraged me to continue practicing Docker and learn more about building reliable cloud applications.
