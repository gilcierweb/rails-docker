# Ruby on Rails, PostgreSQL, Redis, Vue.js with Docker and Docker Compose 

Skills
- Ruby
- Ruby on Rails
- PostgreSQL
- Redis
_ Node.js
- Vue.js
- webpack
- Docker
- Docker Compose

### Setup Docker and Docker Compose
https://docs.docker.com/engine/install/

https://docs.docker.com/compose/install/

### Usage

```shell script
git clone https://github.com/gilcierweb/rails-docker.git

cd rails-docker

docker-compose build

docker-compose run --rm app rails new ./ -d postgresql --webpack=vue

sudo chown -R $USER:$USER . 

cp database.example.yml config/database.yml

docker-compose run --rm app bundle exec rails db:create db:migrate

# case errors gem not install
docker-compose run --rm app bundle install
# case errors with yarn dependencies
docker-compose run --rm app yarn install --check-files 

docker-compose up

# run http://localhost:3000
```
Run http://localhost:3000

### Site
https://gilcierweb.com.br

https://gilcierweb.com.br/posts/dockerizando-uma-aplicacao-ruby-on-rails-com-postgresql-redis-e-vue-js