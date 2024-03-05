# postgres-docker
Postgres DB and pgadmin with Docker Compose.

## Setup postgres and pgadmin
1. Obtain the following images:
    - `docker pull postgres:14.5` following instructions [here](https://www.docker.com/blog/how-to-use-the-postgres-docker-official-image/).
    - `docker pull dpage/pgadmin4:latest`
2. Edit compose.yaml file as described [here](https://github.com/docker/awesome-compose/tree/master/postgresql-pgadmin).
4. Edit the .env file for updating variables. Locate this in the same directory as the compose yaml configuration.
5. From the directory containing the `.env` and the `compose.yaml` files type: `docker compose up`

### Connect pgadmin to postgres
1. Navigate to [localhost:5050](http://localhost:5050) and log in using the criteria set in the `.env` file.
2. Under "Quick Links" click on "Add Server" and a "Register - Server" window appears.
3. In the "General" tab, define a "Name" for the server, e.g. "test-server", could be anything.
4. In the "Connections" tab, set host name/address to be "postgres" (Docker will resolve this to be the container name specified in `compose.yaml`).
5. Populate other fields as described [here](https://github.com/docker/awesome-compose/tree/master/postgresql-pgadmin#add-postgres-database-to-pgadmin).
