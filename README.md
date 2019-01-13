# Rubicure-graphql

Rubicure-graphql is Precure, Japanese battle heroine "Pretty Cure (Precure)" GraphQL implementation based on [Rubicure gem](https://rubygems.org/gems/rubicure).

## Requirements

* ruby >= 2.4.4

* rails >= 5.2.1

## Dependencies

* rubicure >= 1.1.7

## How to deploy

### Using docker-compose

```
$ docker-compose build
$ docker-compose run --rm app bundle install
$ docker-compose up -d
```

### Deploy to heroku

With Heroku CLI

```
$ heroku login
$ heroku create
$ git push heroku master
```

## How to use

Call from your GraphQL client. For your convenient, this app including rails-graphiql, access http(s)://(hostname):(port)/graphiql to try API in GraphiQL.

## You can try Rubicure-graphql in GraphiQL
[https://rubicure-graphql.herokuapp.com/graphiql](https://rubicure-graphql.herokuapp.com/graphiql)

## How to contribute

1. Fork this repo
2. Fun with this code
3. Make pull request
