# Laravel GraphQL Trial

Application to try out creating GraphQL API Server.

Built with PHP and Laravel.

## Requirements

- PHP 7.3.1
- Composer
- [Laravel](https://laravel.com/) 5.7
- SQLite

## Installation

Clone Project

```sh
git clone https://github.com/taiyeoguns/laravel-graphql-trial.git
```

Install Composer dependencies

```sh
composer install
```

Maintain database details in `.env` file

```sh
cp .env.example .env
```

Create SQLite database

```sh
touch database/database.sqlite
```

Migrate and seed database tables

```sh
php artisan migrate && php artisan db:seed
```

Generate app key and start server

```sh
php artisan key:generate && php artisan serve
```

Launch browser

Navigate to `http://localhost:8000/graphql-playground`

### Sample Request

In GraphQL Playground, enter the following sample request:

```graphql
query {
    users(count: 5) {
        data {
            id
            first_name
            last_name
            email
            phone
            created_at
            updated_at
        }
    }
}
```

## Tests

In command prompt, run:

```sh
vendor\bin\phpunit --testdox
```

## Further Information

- [https://medium.freecodecamp.org/graphql-in-laravel-done-right-9cf123d5601b](https://medium.freecodecamp.org/graphql-in-laravel-done-right-9cf123d5601b)
- [https://medium.com/@sadnub/migrating-to-graphql-on-laravel-with-lighthouse-42bd96d9d73](https://medium.com/@sadnub/migrating-to-graphql-on-laravel-with-lighthouse-42bd96d9d73)
- [https://www.howtographql.com/](https://www.howtographql.com/)
