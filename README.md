# graphql-storm
Build your own GraphQL API with Docker, Node, and Postgres

## How to use this repo
This repository is organised into different branches that represent different evolutions of the codebase. You can view the documentation and code from the beginning by selecting the beginning by selecting the `01-beginning` branch.

## The Docker Compose
Docker compose allows us to express a constellation of interconnected microservices. To stand up a local GraphQL API we employ three:

* db/ postgres container listens on port 5432. serves the 
* server/ node server that runs postgraphile. listens on 8080 and connects to db container

## Postgres

The [SQL file](https://raw.githubusercontent.com/graphile/postgraphile/master/examples/forum/schema.sql) used to seed the database is from the postgraphile forum [tutorial](https://github.com/graphile/postgraphile/blob/master/examples/forum/TUTORIAL.md).

## Node Server

The container that runs postgraphile on node js. Start simple. Please inspect the code in `server/Dockerfile`. More information is available in the [Quick Start Guide](https://www.graphile.org/postgraphile/quick-start-guide/).

See http://0.0.0.0:5000/graphiql

For more on how port mapping works in docker see [this article](https://medium.freecodecamp.org/expose-vs-publish-docker-port-commands-explained-simply-434593dbc9a3)