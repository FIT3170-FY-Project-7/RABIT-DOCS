# Manual installation (production)

This method is suited for production instances that does not require Docker.

# Before you begin

Make sure you completed all steps in the [first steps](./first-steps.md) page.

## Requirements

- [Node.js](https://nodejs.org) - version 18 or later
- [MySQL](https://dev.mysql.com/downloads/installer/) - version 8

Other versions may work, but is untested.

## Set up environment variables

In `RABIT-BACKEND`, copy `.env.example` file to `.env`

```
cp .env.example
```

See the [Firebase page](./firebase.md) for more information on setting up Firebase.

## Installation

### Database

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

### Backend

In `RABIT-BACKEND` directory:

Install dependencies

```
npm install --save-dev
```

Compile:

```
npm run build
```

The build artefacts are located at `dist` directory. You can run it with Node:

```
node dist/index.js
```

### Frontend

In `RABIT-FRONTEND` directory:

Install dependencies

```
npm install --save-dev
```

Compile:

```
npm run build
```

The build artefacts are located at `dist` directory. These files can then be hosted using a web server like Apache or nginx.

The following shows a basic nginx configuration, with files located in `/var/www/rabit`. Note that this should only be used as a starting point, and you should make tweaks to suit your setup, such as adding HTTPS.

```nginx
{{ #include ../code/prod-base-example.nginx }}
```
