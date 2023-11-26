# Installation

## Clone project

```sh 
git clone https://github.com/foxmark/docker-rabitmq-base.git
```

## Change directory

```sh
cd docker-rabitmq-base
```

## Edit Configuration

#### Copy and Inspect ```.env``` file and make config changes

```sh
cp .env.example .env
```

```sh
nano .env
```

## Start docker services

```sh
docker-compose up
```

> Note: use ```-d``` to fee the terminal

## Validate installation

Run:

```sh
docker ps --all
```
Output should look a bit like this:

```
CONTAINER ID   IMAGE                     COMMAND                  CREATED          STATUS                      PORTS                                                  NAMES
0b58e20d0162   rabbitmq:3.8.9-management     "docker-entrypoint.s…"   12 minutes ago   Up 12 minutes              4369/tcp, 5671-5672/tcp, 15671/tcp, 15691-15692/tcp, 25672/tcp, 0.0.0.0:15672->15672/tcp, :::15672->15672/tcp                                                   rabbitmq_rabbitmq_1
```

## Access admin dashboard

Navigate to [http://localhost:15672](http://localhost:15672)

User and password define in [config/rabbitmq.conf](../master/config/rabbitmq.conf)

> Note: Port ```15672``` is a default value for ```RMQ_PORT``` variable from [.env](../master/.env.example) file.
