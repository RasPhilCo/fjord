fjord
===

**THIS PROJECT IS IN EARLY ALPHA DEVELOPMENT. USE WITH CAUTION.**

Simplified local node/python/ruby app development for MacOS. Powered by [Heroku buildpacks](https://devcenter.heroku.com/articles/buildpacks).

#### Install

```
$ npm install -g RasPhilCo/fjord
```

#### Requirements

- Docker For Mac
- Postgres.app (if you need a postgres server)
- redis (if you need a redis server)

#### Usage

After install, grab the Heroku buildpacks (they are not packaged with fjord).
```
$ fj sync
```

Build your app and start a ready-to-work bash session via `build`:

```
$ fj build --port=<EXPOSED-PORT>
```

Fjord auto-detects the project's languages and their corresponding buildpacks it needs. Dependency mangers bundled with the buildpacks can be used for external dependencies (i.e. not app specific). For example:

```
# node buildpack (includes npm)
$ fj build --port=5000 --npm=nf,nodemon

# python buildpack (includes pip)
$ fj build --port=8080 --pip=honcho

# ruby buildpack (includes gem)
$ fj build --port=3000 --gem=foreman
```

#### Gotchas

Since DockerForMac runs in a VM, you'll need to update your development database from `localhost` to `docker.for.mac.localhost` to hit Postgres.app or other running services on localhost. Project env vars are easily managed (and more secure!) with a manager like dotenv.
