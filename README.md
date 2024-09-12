# Msox backend

## Technical stack

- Ruby version: 3.3.1
- Rails version: 7.1.3
- Database: Mysql 8.0 (Microsoft Azure MySQL)
- Docker, Docker compose
- Rubocop-rails
- Rspec-rails
- Nginx >= 1.25

## How to start

- Install Docker, Docker compose

  - https://www.docker.com/get-started/
  - https://docs.docker.com/compose/


- Checkout to branch code `develop` for newest code

   ```bash
   git checkout develop
   git pull origin develop
   ```

- Check content of `.env` `.env.sample` for local ENV

- Run command to start containers

   ```bash
   docker compose build
   docker compose up -d
   ```

- Run command to setup rails

   ```bash

   docker compose exec rails db:create
   docker compose exec rails db:migrate
   docker compose exec rails db:seed
   ```
