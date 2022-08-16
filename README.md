## Back-end and Front-end docker compose project


### Getting started

You must add inside your hosts `/etc/hots`

```
127.0.0.1       backend.com.br
127.0.0.1       frontend.com.br
```

Build the project with the next commands

```sh
cp .env.example .env
```

```sh
cp /app/.env.example /app/.env
```

```sh
docker-compose up
```

```sh
docker-compose run --rm composer install
```

```sh
docker-compose run --rm artisan migrate
```
### Commands

You can use all composer, artisan and npm commands with the next commands.

Run composer commands
```sh
docker-compose run --rm composer
```
Run artisan commands
```sh
docker-compose run --rm artisan
```
Run npm commands
```sh
docker-compose run --rm node
```