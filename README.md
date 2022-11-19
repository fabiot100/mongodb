# MongoDB

This repository contains some essential files that can be used for deploy the MongoDB container, using Swarm.

## Preparations

Rename the **env/mongodb.env_example** and **env/mongodb-express.env_example** files to **env/mongodb-express.env** and **env/mongodb-express.env** and change the parameters correctly.

Create a secret for MongoDB named "mongodb" using the secret_example.txt file. Remember: before create the secret, change the parameters according with you wish:

```shell
docker secret create mongodb secret_example.txt
```

## Deploy

To deploy the stack using Swarm, just follow the command below:

```shell
docker stack deploy --compose-file docker-compose.yml mongodb
```