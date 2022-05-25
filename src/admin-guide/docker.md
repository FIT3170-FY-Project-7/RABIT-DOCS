# Deployment with Docker

## Requirements

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Installation

1. Clone the repository. We use git submodules so make sure you also cloned all submodules:
```
$ https://github.com/FIT3170-FY-Project-7/RABIT-COMMON
```
2. Build and run the container. This may take a while.
```
$ docker-compose up -d
```
3. Visit http://localhost:8080 (frontend) and http://localhost:8000 (backend) to check that the container is properly
deployed.

## Update 
````
$ git pull --recurse-submodules
$ docker-compose up -d --build --force-recreate
$ docker image prune -f
````

## Uninstall
Remove the container without deleting database data:
```
$ docker-compose down
```

Remove the container and delete all data:

**WARNING: this will delete all plots, accounts and everything else stored in the database. This operation is irreversible.**
```
$ docker-compose down -v
```