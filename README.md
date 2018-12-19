## Todo list app
### In this project I used:
 - Node & Express
 - GraphQL
 - Apollo (Client-Server)
 - Typescript
 - React/Redux
 - Docker
 - Github
 
### Docker instructions:
Run project with _docker-compose_:

    docker-compose up

Run project with docker cli

    docker network create todo-network
    docker build --tag todo-mongo:1 db
    docker run --name todo-mongo-container --net todo-network todo-mongo:1
    docker build --tag todo-server:1 server
    docker run --name todo-server-container --net todo-network --publish 3000:3000 todo-server:1
    docker build --tag todo-client:1 client
    docker run --name todo-client-container --net todo-network --publish 4000:3001 todo-client:1

**After running the above docker commands, the todo app is available in host machine at http://localhost:4000/**
