<p align="center">
  <a href="https://cdn.ednsquare.com/s/*/4a103e29-8bfb-467c-b2f6-1e510638e9fc.png" target="blank"><img src="https://cdn.ednsquare.com/s/*/4a103e29-8bfb-467c-b2f6-1e510638e9fc.png" width="200" alt="Go" /></a>
</p>

<h1 align="center">Golang Example Boilerplate</h1>

<p align="center">
  <a href="https://github.com/saefullohmaslul/golang-example/actions?query=workflow%3Alint" target="_blank"><img src="https://github.com/saefullohmaslul/golang-example/workflows/lint/badge.svg?branch=master" alt="build" /></a>
  <a href="https://github.com/saefullohmaslul/golang-example/actions?query=workflow%3Atest" target="_blank"><img src="https://github.com/saefullohmaslul/golang-example/workflows/test/badge.svg?branch=master" alt="license" /></a>
  <a href="https://codecov.io/gh/saefullohmaslul/golang-example/tree/master/src" target="_blank"><img src="https://codecov.io/gh/saefullohmaslul/golang-example/branch/master/graph/badge.svg" alt="license" /></a>
  <a href="https://goreportcard.com/report/github.com/saefullohmaslul/golang-example" target="_blank"><img src="https://goreportcard.com/badge/github.com/saefullohmaslul/golang-example" alt="license" /></a>
  <a href="https://github.com/saefullohmaslul/golang-example/actions?query=workflow%3Abuild" target="_blank"><img src="https://github.com/saefullohmaslul/golang-example/workflows/build/badge.svg?branch=master" alt="license" /></a>
  <a href="https://opensource.org/licenses/MIT" target="_blank"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="license" /></a>
</p>

## Feature

- Clean code (DDD)
- Gin Framework
- Docker and docker-compose
- ORM with gorm
- Pub/Sub with kafka
- Integration testing
- Integration with github actions

## How to run

There are two ways to run this application, with docker or without docker

```bash
# running with docker

# copy .env
cp .env.example .env

# running in development mode, you can use live-reload when safe file
make run-local

# remove production container
make down-local


# running in production image
make run-production
docker logs --tail=100 -f golang_example_production # monitoring production container
docker exec -it golang_example_production sh # access bash on production container

# remove production container
make down-production
```

```bash
# running in local/without docker

# copy .env
cp .env.example .env
make install
make run
```

## Run tests

```bash
make test
```

## Run lint

```bash
make lint
```

## Project structure

```bash
.
├── air.conf                              # air configuration (like nodemon.json)
├── docker-compose.production.yml         # docker compose for production image
├── docker-compose.yml                    # docker compose for local image
├── Dockerfile                            # build app image
├── go.mod                                # go mod
├── go.sum                                # go sum
├── LICENSE                               # license for this boilerplate
├── Makefile                              # contain all command to run project
├── README.md                             # you read this file
├── src
│   ├── app                               # application configuration
│   ├── controllers                       # all controller in here
│   ├── database                          # contain entity, migation and database instance
│   │   ├── connection.go
│   │   ├── entity
│   │   └── migration
│   ├── main.go                           # main project
│   ├── middlewares                       # all middleware configuration
│   ├── repository                        # repository (handler query database)
│   ├── routes                            # all routes which is application need
│   ├── services                          # contain all business logic
│   ├── utils                             # utility application
│   └── validation                        # validation request schema
└── __tests__                             # contain all integration testing file
```

## Stay in touch

* Author - [Saefulloh Maslul](https://linkedin.com/saefullohmaslul)

## License

Golang-Example is [MIT](LICENSE).
