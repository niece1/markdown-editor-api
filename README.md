![GitHub language count](https://img.shields.io/github/languages/count/niece1/markdown-editor-api)
![GitHub top language](https://img.shields.io/github/languages/top/niece1/markdown-editor-api)
![GitHub repo size](https://img.shields.io/github/repo-size/niece1/markdown-editor-api)
![GitHub contributors](https://img.shields.io/github/contributors/niece1/markdown-editor-api)
![GitHub last commit](https://img.shields.io/github/last-commit/niece1/markdown-editor-api)
![GitHub](https://img.shields.io/github/license/niece1/markdown-editor-api)

## Intro

Development in progess. This repo is an example how create markdown editor tool using Laravel (api only).

## Usage

If it happens you decide to run it on your machine make sure you have [Docker installed](https://docs.docker.com/docker-for-mac/install/).

Clone repository.

From your terminal window at the project root spin up the containers for the web server by running
```
docker-compose up -d --build
```
The following are built for our web server, with their exposed ports detailed:

- **nginx** - :8088
- **mysql** - :4306
- **php** - :9000
- **phpmyadmin** - :8081
- **mailhog** - :8025

Depending on operating system, you may encounter rights problems so make sure you have appropriate writable rights for project folder.

To generate APP_KEY run:
```
docker-compose exec php php artisan key:generate
```

To install dependencies run command:
```
docker-compose exec php composer install
```

In your **.env** file fill in variables related to database, especially pay attention to DB_HOST to be specified as mysql.

MAIL_HOST should be specified as mailhog.

To perform database migrations run:
```
docker-compose exec php php artisan migrate
```

## Technical features

```
- Sanctum/Fortify authentication (all features, including two-factor one)
- Api
```

## License

This is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
