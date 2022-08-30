# Deployment with Docker

## Before you begin

Make sure you completed all steps in the [first steps](./first-steps.md) page.

## Requirements

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Set up environment variables

In `RABIT-BACKEND`, copy `.env.example` file to `.env`

```
cp .env.example
```

Then fill out the database environment variables as follows:

```shell
DB_HOST=db
DB_USER=root
DB_PASSWORD=replace-this
DB_NAME=rabit
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

## Installation

In the `RABIT-COMMON` directory, run:

```
docker-compose up --build
```

The app will be running at <http://localhost:8080/>

In case of `npm` error, you may need to return to `RABIT-FRONTEND` and/or `RABIT-BACKEND` and run:

```
rm package-lock.json
rm -rf node_modules
npm install
```

Afterwards, return to `RABIT-COMMON` and re-run `docker-compose up --build`

When you are making changes to the code, stop the containers and run

```
docker-compose up --build --force-recreate
```

Doing this will force rebuild and recreate the docker containers.
