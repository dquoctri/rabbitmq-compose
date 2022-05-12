# rabbitmq-compose
RabbitMQ architecture and essential components

rabbitmq-plugins list

# [Docker](https://docs.docker.com/get-started/overview)
> Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. With Docker, you can manage your infrastructure in the same ways you manage your applications. By taking advantage of Docker’s methodologies for shipping, testing, and deploying code quickly, you can significantly reduce the delay between writing code and running it in production.

# [Docker Compose](https://docs.docker.com/compose/)
> Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML file to configure your application’s services. Then, with a single command, you create and start all the services from your configuration.

# Prerequisities
## Docker and docker-compos
Docker and docker-compose are required in order to run this app successfully
* docker >= 19.03.0+
* docker-compose

You can download and install Docker on multiple platforms. Refer to the [following section](https://docs.docker.com/get-docker/) and choose the best installation path for you.

Check the version of docker to make sure docker is installed

```
docker --version
```
> Docker version 20.10.7, build f0df350

# Quick Start

Clone this repository first:

```
git clone https://github.com/dquoctri/rabbitmq-compose.git
cd rabbitmq-compose
```
The following commands need to be run docker compose:

```
docker compose up -d
```
# Details
## Code structure

Here’s a documentation project structure

## docker-compose.yml

```
version: '3.9'

services:

networks:
  env_net:
    external: true
    driver: bridge

volumes:
  datadir: # external: true
  
```

## Note
> Both **$VARIABLE** and **${VARIABLE}** syntax are supported. Additionally when using the 2.1 file format, it is possible to provide inline default values using typical shell syntax:
> 
> - **${VARIABLE:-default}** evaluates to `default` if `VARIABLE` is unset or empty in the environment.
> - **${VARIABLE-default}** evaluates to `default` only if `VARIABLE` is unset in the environment.
> 
> Similarly, the following syntax allows you to specify mandatory variables:
> 
> - **${VARIABLE:?err}** exits with an error message containing `err` if `VARIABLE` is unset or empty in the environment.
> - **${VARIABLE?err}** exits with an error message containing `err` if `VARIABLE` is unset in the environment.
> 
> Other extended shell-style features, such as **${VARIABLE/foo/bar}**, are not supported.
> 
> You can use a `$$` (double-dollar sign) when your configuration needs a literal dollar sign. This also prevents Compose from interpolating a value, so a `$$` allows you to refer > to environment variables that you don’t want processed by Compose.

## Environments

Set environment variables used by the system in ./*.env file (Copy the sample in `.env` file, example: `dev.env`, `prod.env` and `.env` by default) with specific version of [Microsoft SQL Server](https://hub.docker.com/_/microsoft-mssql-server) images. 


```


```

