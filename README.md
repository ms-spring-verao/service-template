# Chassis

This is a basic service [Chassis][chassis] for SpringBoot services within Pingr.

## How to use it

The code boilerplate contains a few information that **must be replaced** with real values. To identify them, run on the root directory of this chassis:

```sh
grep "CHASSIS" . -R
```

As of the date this document is being written, the spots are:

```plain
./src/main/resources/application.yml:      group-id: CHASSIS-GROUP-ID
./src/main/resources/application.yml:    url: jdbc:postgresql://localhost:CHASSIS-PG-HOST-PORT/CHASSIS-DB-NAME
./src/main/resources/application.yml:  port: CHASSIS-PORT
./docker-compose.yaml:  CHASSIS-PG-CONTAINER-NAME:
./docker-compose.yaml:      - CHASSIS-PG-HOST-PORT:5432
```


[chassis]: https://microservices.io/patterns/microservice-chassis.html
