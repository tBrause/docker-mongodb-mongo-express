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

**Container Name**

- con-mongodb
- con-mongo-express

**Restart**

- always

**PORTS**

- 27017 (MongoDB)
- 8081 (Mongo-Express)

**Networks**

- net-mongodb (driver: bridge)