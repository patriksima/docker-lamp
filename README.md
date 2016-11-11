# LAMP stack Docker

Apache: 2.4

PHP: 7.0

MySQL: 5.7

## Requirements

Git

Docker

Docker Compose

## Installation

Add this repository into your project root directory:

```bash
git submodule add https://github.com/wrongware/docker-lamp.git
```

## Setup

You can configure packages in docker-compose.yml file:

```bash
                - INSTALL_NPM=true
                - INSTALL_GULP=true
                - INSTALL_COMPASS=true
                - INSTALL_COMPOSER=true
                - INSTALL_WPCLI=true
```

## MySQL credentials

User: dev

Pass: secret

Database name: myapp

Root pass: root

## Usage

1. In the docker-lamp directory run:

```bash
docker-compose up -d apache mysql
```

2. Enter into Apache container as root user, to execute commands like (WP-Cli, Composer, PHPUnit, Gulp, ...).

```bash
docker-compose exec apache bash
```

or

```bash
docker-compose exec --user=wrongware apache bash
```

## Documentation

List current running Containers

```bash
docker ps
```

You can also use the this command if you want to see only this project containers:

```bash
docker-compose ps
```

Close all running Containers

```bash
docker-compose stop
```

To stop single container do:

```bash
docker-compose stop {container-name}
```

Delete all existing Containers

```bash
docker-compose down
```
