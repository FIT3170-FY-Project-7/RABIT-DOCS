# Backend

## Overview

As we are using a controller-service-repository architecture, the backend has its functions modularised into these concepts.

Example of the file hierarchy Controller -> Service -> Repositories:

![1666253494115](image/backend-architecture/1666253494115.png)

Sets of controller/service/repository files for different business logic functionalities have been separated into their own directories. This is to keep the code self-contained, and maintainable. The directories can be seen below:

![1666253504685](image/backend-architecture/1666253504685.png)

Plot – Focuses on the business logic for plotting and visualising data.

RawData – Focuses on the business logic for receiving and processing user uploaded files.

User – Focuses on user related business logic, (i.e login, signup).

## Controller-Service-Repository

The controller will contain the REST API definitions and then apply the outcome of those to a service function. The REST APIs are created using the “express” ts library, which is initialised in the index.ts and router.ts files.

Index file:

 ![1666253585367](image/backend-architecture/1666253585367.png)

Router.ts:

 ![1666253591613](image/backend-architecture/1666253591613.png)


Example of creating REST API with express

![1666253600455](image/backend-architecture/1666253600455.png)


More on express can be found at: https://expressjs.com/ 

The service function implements the business logic and functionality and then applys the outcome of those to the repository logic if needed.

The repository manages communications to the database with SQL queries. The SQL queries are managed using the “mysql12” library which is initialised in the databaseConnections.ts file. The connection details that are used to initialise the library can be found in the .env file.

databaseConnections.ts file:

 ![1666253898514](image/backend-architecture/1666253898514.png)


.env file with password redacted:

![1666253906306](image/backend-architecture/1666253906306.png)
