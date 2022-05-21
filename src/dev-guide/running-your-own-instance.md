# Running your own RABIT instance

## Why would I want to do this?

There are several reasons why you would want to run your own instance instead of using [our public one](https://rabit2022.cloud.edu.au/):

- Some organisations may restrict data from going outside thwir network for security and confidentiality reasons. Deploying your own RABIT instance ensures you have full control on where and how the data is transmitted and stored.
- You have a limited internet bandwidth but good local network bandwidth.
- You are developing RABIT itself and want to test your improvements. One does not simply test in production, right?

## Deployment instructions

We offer various ways of deployment:

### Docker

#### Requirements

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

#### Installation

1. Clone the repository. We use git submodules so make sure you also cloned all submodules:
```
$ https://github.com/FIT3170-FY-Project-7/RABIT-COMMON
```
2. Build and run the container. This may take a while.
```
$ docker-compose up -d
```
3. Visit http://localhost:8000 to check that the container is properly deployed.

#### Update 
````
$ git pull --recurse-submodules
$ docker-compose up -d --build --force-recreate
$ docker image prune -f
````

#### Uninstall
Remove the container without deleting database data:
```
$ docker-compose down
```

Remove the container and delete all data:
```
$ docker-compose down -v
```

### Manual installation
