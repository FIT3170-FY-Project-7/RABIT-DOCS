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

For Firebase variables, go to your project settings and scroll down to the app you just registered. Then fill out the
variables as follows:

```shell
FIREBASE_API_KEY="" # firebaseConfig.apiKey
FIREBASE_AUTH_DOMAIN="" # firebaseConfig.authDomain
FIREBASE_PROJECT_ID="" # firebaseConfig.projectId
FIREBASE_STORAGE_BUCKET="" # firebaseConfig.storageBucket
FIREBASE_MESSAGING_SENDER_ID="" # firebaseConfig.messagingSenderId
FIREBASE_APP_ID="" # firebaseConfig.appId
```

Any variables not listed above should not be changed, unless you understand the ramifications and how to deal with any
issue that may arise.

### Database

Set up the database by running `DB_generation_schema.sql` in `RABIT-BACKEND/database-schemas`.

### Creating a temporary user

This user allows you to upload immediately without having to create an account first.

You can do this by running `create_temp_user.sql` script in `RABIT-BACKEND/database-schemas`.

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
