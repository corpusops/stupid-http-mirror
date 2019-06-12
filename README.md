# unconditionnal and stupid http caching mirror

- docker-compose based setup to cache arbitrary http/https mirror
- You can use those env vars (defaults):
    - ``MIRRORED_SCHEME``: http://
    - ``MIRRORED``: download.geofabrik.de
    - ``EXPIRY``: 172800 (in seconds)

```sh
cp .env.dist .env
$EDITOR .env
docker-compose run --rm mirror
# docker-compose -f docker-compose.yml -f docker-compose-prod.yml up -d --force-recreate
```

- set arg: ``nocache=1`` to bypass cache
- set method: ``PURGE`` to invalidate the cache.
