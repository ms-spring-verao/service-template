# Service Template

This is a basic service [Service Template][template] for SpringBoot services within Pingr.

## How to use it

### Remove Chassis placeholders

> For further information on Chassis pattern, check [this page][chassis]

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

### Edit business logic boilerplate

As of the date this document is being written, the spots are:

```plain
.
├── application
|   ├── KafkaConsumerConfig.java
|   └── KafkaConsumerService.java
└── core
    ├── Account.java
    ├── AccountRepository.java
    ├── events
    │   ├── AccountCreatedEvent.java
    │   └── AccountDeletedEvent.java
    └── services
        └── SynchronizeAccount.java
```


[chassis]: https://microservices.io/patterns/microservice-chassis.html
[template]: https://microservices.io/patterns/service-template.html

