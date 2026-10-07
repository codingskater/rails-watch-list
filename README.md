# Rails Watch List

A Rails application for organizing movie watch lists.

App: https://watch-list-coding-skater-3363ce5d5852.herokuapp.com/

## Requirements

- Ruby 3.3.5 (see `.ruby-version`)
- Bundler
- PostgreSQL, running locally

The development and test databases use the names `rails_watch_list_development` and `rails_watch_list_test`. The default database configuration connects to PostgreSQL as your local operating-system user, without a password. Make sure that PostgreSQL has a matching role that can create databases, or update `config/database.yml` for your local PostgreSQL credentials.

## Set Up and Run

From the project directory, run:

```sh
bin/setup
```

This installs the Ruby dependencies, prepares the development database, clears old logs and temporary files, and starts the development server. When it creates a new database, Rails runs the seed task, which needs an internet connection to fetch movie data. Open [http://localhost:3000](http://localhost:3000).

To prepare the application without starting the server:

```sh
bin/setup --skip-server
bin/dev
```

Stop the server with `Ctrl+C`.

## Database and Sample Data

`bin/setup` runs `bin/rails db:prepare`, which creates the development database if needed and applies migrations. To apply later migrations manually, run:

```sh
bin/rails db:migrate
```

To reload the sample movies manually, run:

```sh
bin/rails db:seed
```

Seeding requires an internet connection to fetch movie data. It deletes existing movie records before loading the sample movies.

## Tests

Run the RSpec suite with:

```sh
bundle exec rspec
```
