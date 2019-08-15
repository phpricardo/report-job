# Jobs no Rails com Redis

Tutorial da aplicação da utilização de jobs no rails.

## Stack Utilizada

* Ruby 2.6.3
* Rails 5.2.3
* Redis (Via Docker Imagem 5.0.5-alpine)
* Sidekiq (gem)

## Setup do Projeto

Executar o servidor do Redis

`redis-server`

> Como dito, o redis foi utilizado via uma imagem oficial baixada do docker hub

Clonar o repositório:

`git clone <repositorio>`

Executar comando:

`bundle install`

Suba o servidor rails:

`rails s`

Suba o servidro Sidekiq

`bundle exec sidekiq -q reports -c 8`

Acessar a URL:

`http://localhost:3000/reports`

Acessar a URL do servidor Redis:

`http://localhost:3000/sidekiq/`

