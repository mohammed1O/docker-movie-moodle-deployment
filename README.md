# docker-movie-moodle-deployment
Docker Compose and Swarm deployment for a multi-service project including a Flask web app with MongoDB, Neo4j, Redis, Moodle with MariaDB, and supporting services for scalable and highly available infrastructure


A  project designed to explore Docker concepts and techniques by deploying three parts using a single docker-compose file, with scalability and high availability through Docker Swarm.

The three parts of the project:
App:

A simple Python Flask web application.

Uses three databases:

MongoDB (for storing data)

Neo4j (for storing relationships between users and favorite movies)

Redis (as a cache to improve performance)

An Apache server to serve static images used by the app.

An SMTP server included to demonstrate email service deployment (though not currently sending emails).

Moodle:

A Moodle instance with its own MariaDB database.

Base:

Enables publishing the web app and other services outside the Docker network for external access.

Key points:
All services are managed via a single docker-compose file divided into three sections.

Volumes are used to persist database data, ensuring data durability if containers fail.

Backup files and restore procedures are provided for initial database setup inside Docker volumes.

The final goal is to deploy the stack using Docker Swarm to allow high availability and service scalability.
