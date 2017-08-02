# docker-suicide

An [HTTP](https://github.com/behance/docker-nginx)-serving container that will properly respond to healthchecks at `/` until `LIFESPAN` seconds, before killing itself.

Useful to test cluster configurations where shuffling containers can cause bursts in orchestration logic.

NOTE: healthchecks are

### Environment Variables

Variable | Default | Description
--- | --- | ---
LIFESPAN | 60 | How long the container will properly respond to healthchecks before killing itself
RANDOM_MIN | 0 | Combined with RANDOM_MAX, will randomize a value to add to LIFESPAN
RANDOM_MAX | 0 | Combined with RANDOM_MIN, will randomize a value to add to LIFESPAN

