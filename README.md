# Docker based MySQL and PHPMyAdmin

This repo is used for setting up new standalone MySQL server with PHPMyAdmin for development use cases.

## How to setup

Make sure you have docker installed and follow the steps

- Clone the repo
- Update MySQL docker image version in `docker-compose.yml` if you need older version.
- Run `docker compose --env-file .env up -d --build`
- Open localhost with `PMA_PORT` to access PhpMyAdmin login page.
- Optionally you can put files inside `.Docker/files` folder to access them inside MySQL container

## Debugging
Sometimes the config set on the server is not optimized for importing large files, in this case uncomment the config line in `docker-compose.yml` if your large import is failing with error `mysql server gone away`
