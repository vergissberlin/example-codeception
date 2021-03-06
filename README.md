# Codeception example project

## Requirements

- codeception
- php
- php-mbstring
- docker => 1.11.2
- docker-compose => 1.7.1

## Included

- selenium server
- chrome linux64 webdriver

## Run the tests

1. Starting the webserver ``php -S localhost:8090``
- Run acceptance test ``codecept run acceptance``

## With selenium

- Start selenium hub and register clients
- The _docker-compose_ is taken from https://github.com/elgalu/docker-selenium/

````bash
export SELENIUM_HUB_PORT=4444 NODES=3 VNC_FROM_PORT=40650 VNC_TO_PORT=40700 VIDEO=false
docker-compose -p grid up -d
docker-compose -p grid scale chrome=${NODES} firefox=${NODES}
````

# Next

- Running parralel http://codeception.com/docs/12-ParallelExecution
- Functional tests
- Unit tests
