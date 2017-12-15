fjord
===

Simplified local node app development for MacOS. Powered by [Heroku buildpacks](https://devcenter.heroku.com/articles/buildpacks).

#### Install

`$ yarn global add @rasphilco/fjord`

#### Requirements

- Docker For Mac
- Postgres.app (if you need a postgres server)
- Redis Desktop Manager (if you need a redis server)

#### Run

Build your app and open a ready-to-work bash session via `fj start <EXPOSED-PORT> <GLOBAL-NPM-DEPS>...`. For example:

`$ fj start 8000 foreman`

#### Gotchas

Since DockerForMac runs in a VM, you'll need to update your development database `localhost` to `docker.for.mac.localhost` to hit Postgres.app or other running services on localhost.
