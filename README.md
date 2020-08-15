# Standalone Sidekiq Web

Launch a standalone Sidekiq Web dashboard via Docker

## Build

```
$ docker build -t sidekiq-web:dev .
```

## Run

```
$ docker run -p 9292:9292 -e REDIS_URL=<the redis url> -it meoooh/standalone-sidekiq-web
```

## Configuration

```
REDIS_SIZE: Concurrency setting (default: 1)
REDIS_URL: The redis host URL (default: redis://localhost:6379/0)
SIDEKIQ_CRON: Set to true to enable the Sidekiq Cron view (default: false)
SIDEKIQ_USERNAME: HTTP Basic Auth username
SIDEKIQ_PASSWORD: HTTP Basic Auth password
```

**NOTE:** To enable HTTP Basic Auth you must set BOTH `SIDEKIQ_USERNAME` and `SIDEKIQ_PASSWORD`.
