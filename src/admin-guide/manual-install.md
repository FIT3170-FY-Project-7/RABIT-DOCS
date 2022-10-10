# Manual installation

## Before you begin

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

Then fill out the following variables according to your MySQL configuration:

```shell
DATA_PATH= # location of uploaded files
DB_HOST= # MySQL host
DB_USER= # MySQL user
DB_PASSWORD= # MySQL password
DB_NAME= # database name
```
See the [Firebase page](./firebase.md) for more information on setting up Firebase.

Any variables not listed above should not be changed, unless you understand the ramifications and how to deal with any
issue that may arise.

### Database

Run `DB_generation_schema.sql` in `RABIT-BACKEND/database-schemas` to initialise all tables. Then, run
`create_temp_user.sql` from the same directory to create the temporary user which will be associated with all uploaded
data.

```
mysql -u <DB_USER> -p<DB_PASSWORD> <DB_NAME> < DB_generation_schema.sql
mysql -u <DB_USER> -p<DB_PASSWORD> <DB_NAME> < create_temp_user.sql
```

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
