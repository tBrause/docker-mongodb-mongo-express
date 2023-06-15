# MongoDB und Mongo-Express mit Docker

## Images

- mongo:4.2
- mongo-express

## Installation

> CMD: Projektordner erstellen und hinein wechseln

    mkdir Name; cd Name

> CMD: git clone & git remote

    git clone https://github.com/tBrause/docker-mongodb-mongo-express .; git remote remove origin;

## Docker-Compose starten

> CMD: docker-compose

    docker-compose up -d

## Zugang zu Mongo-Express

- [http://localhost:8081](http://localhost:8081)
- Benutzer: admin
- Passwort: tribes

## Konfiguration

### Container Name

- con-mongodb
- con-mongo-express

### Volumes

- ./data:/data/db

### Environment

#### MongoDB

- MONGO_INITDB_ROOT_USERNAME=admin
- MONGO_INITDB_DATABASE=auth
- MONGO_INITDB_ROOT_PASSWORD=pass

#### Mongo-Express

- ME_CONFIG_MONGODB_SERVER=mongo-dev
- ME_CONFIG_MONGODB_ADMINUSERNAME=admin
- ME_CONFIG_MONGODB_ADMINPASSWORD=pass
- ME_CONFIG_BASICAUTH_USERNAME=admin
- ME_CONFIG_BASICAUTH_PASSWORD=tribes

### Restart

- always

### PORTS

- 27017 (MongoDB)
- 8081 (Mongo-Express)

### Networks

- net-mongodb (driver: bridge)