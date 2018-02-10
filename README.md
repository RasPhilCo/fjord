fjord
===

**THIS PROJECT IS IN EARLY ALPHA DEVELOPMENT. USE WITH CAUTION.**

Simplified local node/python/ruby app development for MacOS. Powered by [Heroku buildpacks](https://devcenter.heroku.com/articles/buildpacks).

#### Install

`$ npm install -g RasPhilCo/fjord`

#### Requirements

- Docker For Mac
- Postgres.app (if you need a postgres server)
- Redis Desktop Manager (if you need a redis server)

#### Run

Build your app and open a ready-to-work bash session via `fj start <EXPOSED-PORT> <OPTIONAL-GLOBAL-LANGUAGE-DEPS>...`. For example:

```
# node
$ fj start 5000 nodemon

# python
$ fj start 8080

# ruby
$ fj start 3000
```

All language builds come with foreman/node-foreman/honcho for running Procfiles.

#### Gotchas

Since DockerForMac runs in a VM, you'll need to update your development database `localhost` to `docker.for.mac.localhost` to hit Postgres.app or other running services on localhost.
