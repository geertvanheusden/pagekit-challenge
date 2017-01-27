# Docker Basics - Docker Compose

## Challenge 1

Create a `docker-compose.yml` file (version 2) and add **mysql** as a service.

Specify the following environment variables for this service:
- MYSQL_ROOT_PASSWORD
- MYSQL_DATABASE

Write the content (`/var/lib/mysql`) to a **mounted** volume (db folder) in the same directory where the `docker-compose.yml` file is located.

## Challenge 2

Add **pagekit** (repository name: pagekit/pagekit) as a secondary service and expose port **80** in the container to **8080*.

Specify a **named** volume:
- `storage` to `/pagekit/storage` in the container

## Challenge 3

Create two networks **pagekitnet_internal** and **pagekitnet_external**. Specify both networks for the **pagekit** service and only **pagekitnet_internal** for the **mysql** service.

## Challenge 4

Start the services and configure pagekit.

## Challenge 5

Add a **backup** service that will create a mysql dump every 5 minutes

Tips: 
 - https://github.com/tutumcloud/mysql-backup
 - Cron: */5 * * * *
