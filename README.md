# Rails api docker template

## Build the new project with the next command

`docker-compose run api rails new . --api -T --force --no-deps --database=postgresql`

## Boot up the project

`docker-compose up -d --build`

## Create the database

`docker-compose run api rails db:create`