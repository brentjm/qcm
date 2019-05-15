# Template web app using docker containers.
Builds Docker containers to run the QCM

## Overview
* *docker-compose.yml*:
  * Creates services with volumes and network
    * Node-RED
    * PostgreSQL
    * Grafana
* *docker_teardown.sh*
  * Removes all containers, images, volumes and networks associated with this repository

## Getting started
1. clone this repository
2. run docker-compose
`$docker-compose up -d`
3. Open browser to localhost:1880
  * In the PostgreSQL flow open the postgres node and edit the defined database.
    * Insert the user and password defined in the postgres/Dockerfile. You should
    change these if you want to deploy externally.
      * user: postgres
      * password: postgrespassword
  * Deploy the flow when done
4. Open browser to localhost:1880/ui
  * operate QCM
4. Open browser to localhost:3000
  * Default username and password:
    * user: admin
    * password: grafana

# Author

**Brent Maranzano**

# License

This project is licensed under the MIT License - see the LICENSE file for details
