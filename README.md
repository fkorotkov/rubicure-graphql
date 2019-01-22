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

You have to set environment values if running in production env.

```
RAILS_ENV=production
SECRET_KEY_BASE=(generate with `docker-compose run --rm app rails secret`)
RAILS_SERVE_STATIC_FILES=true (or enabled)
```

### Deploy to heroku

With Heroku CLI

```
$ heroku login
$ heroku create
$ git push heroku master
```

## How to use

Call from your GraphQL client. For your convenience, this app includes rails-graphiql, access http(s)://(hostname):(port)/graphiql to try API in GraphiQL.

## You can try Rubicure-graphql in GraphiQL

In Heroku

[https://rubicure-graphql.herokuapp.com/graphiql](https://rubicure-graphql.herokuapp.com/graphiql)

or AWS (Elastic Beanstalk)

[https://rubicure-graphql.aws.sastudio.jp/graphiql](https://rubicure-graphql.aws.sastudio.jp/graphiql)

## How to test with head (or another) version of Rubicure gem

1. Clone this repo
2. Checkout "testing_new_precure" branch
3. Fix "Dockerfile" ( branch name, upstream repo )
4. Build your Docker image ( docker-compose build [--no-cache] )
5. Launch the development server ( docker-compose up )

## How to contribute

1. Fork this repo
2. Create your feature branch ( git checkout -b features_or_fix_or_chores_or_something/patch_name )
3. Fun with this code and commit your changes ( git commit -am "I have made some modifications" )
4. Push to your forked repo ( git push origin features_or_fix_or_chores_or_something/patch_name )
5. Create new pull request
