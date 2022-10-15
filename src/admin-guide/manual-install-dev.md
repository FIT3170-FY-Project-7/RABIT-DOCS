# Manual installation (development)

This method is best suited for development environments, for its quicker build times and automatic rebuilding.

## Before you begin

Make sure you completed all steps in the [first steps](./first-steps.md) page.

## Requirements

- [Node.js](https://nodejs.org) - version 18 or later
- [MySQL](https://dev.mysql.com/downloads/installer/) - version 8
  - Alternatively [Docker](https://docs.docker.com/get-docker/) and [Docker Compose](https://docs.docker.com/compose/install/) to run MySQL on Docker container

Other versions may work, but is untested.

## Set up environment variables

In `RABIT-BACKEND`, copy `.env.example` file to `.env`

```
cp .env.example
```

See the [Firebase page](./firebase.md) for more information on setting up Firebase.

## Installation

### Database

#### Running MySQL on the local machine

Fill out the following variables according to your MySQL configuration:

```shell
DATA_PATH= # location of uploaded files
DB_HOST= # MySQL host
DB_USER= # MySQL user
DB_PASSWORD= # MySQL password
DB_NAME= # database name
```

Any variables not listed above should not be changed, unless you understand the ramifications and how to deal with any
issue that may arise.

Run `DB_generation_schema.sql` in `RABIT-BACKEND/database-schemas` to initialise all tables. Then, run
`create_temp_user.sql` from the same directory to create the temporary user which will be associated with all uploaded
data.

```
mysql -u <DB_USER> -p<DB_PASSWORD> <DB_NAME> < DB_generation_schema.sql
mysql -u <DB_USER> -p<DB_PASSWORD> <DB_NAME> < create_temp_user.sql
```

> ⚠️ **WARNING**
>
> Running `DB_generation_schema.sql` will drop all existing tables and thus delete all data in the database.

#### Running MySQL on a Docker container

If you don't want to go through the hassle of installing and setting up MySQL, you can simply run it as a Docker container. This method is somewhat similar to the [Docker deployment method](./docker.md) but without running the frontend and backend containers.

Fill out the database environment variables as follows:

```shell
DATA_PATH=./data
DB_HOST=localhost # NOTE: this is different to the docker production build!
DB_USER=root
DB_PASSWORD=replace-this
DB_NAME=rabit
```

The compose file is located at `db-docker-compose.yml`, which we must pass on every `up` and `down commands.

To deploy MySQL container, run

```
docker-compose up -f db-docker-compose.yml --build
```

This will run the init scripts automatically. You must wait until the log prints
```
[System] [MY-010931] [Server] /usr/sbin/mysqld: ready for connections. Version: '8.0.30'  socket: '/var/run/mysqld/mysqld.sock'  port: 3306  MySQL Community Server - GPL.`
```

at which point the database has been successfully initialised.

### Backend

In `RABIT-BACKEND` directory:

Install dependencies

```
npm install --save-dev
```

Run the app

```
npm run start
```

The backend is now available at <http://locahlost:8000>.

### Frontend

In `RABIT-FRONTEND` directory:

Install dependencies

```
npm install --save-dev
```

Run the app

```
npm run start
```

The app will be running at <http://localhost:3000/>.

## Update

Run `git pull --recurse-submodules` then follow the installation instructions again.

## Uninstall

Remove the database container without deleting database data:

```
docker-compose -f db-docker-compose.yml down
```

Remove the container and delete all data:

> ⚠️ **WARNING**
>
> This will delete all plots, accounts and everything else stored in the database. **This operation is irreversible.**
>
> This does NOT delete any user data in Firebase. Ensure that you deal with this appropriately to avoid any data synchronisation issue in the future.

```
docker-compose -f db-docker-compose.yml down -v
```
