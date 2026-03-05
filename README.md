c3lounger
===

An alternative frontend to c3lounge.de

Install
===

You can use the public image available under `ghcr.io/playlix42/c3lounger:latest`
Alternatively, you can build it from scratch:

```shell
docker build -t name .
```

Example for a docker-compose.yaml:

```yml
services:
  c3lounger:
    image: ghcr.io/playlix42/c3lounger:latest
    ports:
      - "8080:80" # Maps host port 8080 to container port 80
    restart:
      - unless-stopped # or whatever you prefer
```
Replace the `image` section with the name of the local image if you prefer to build locally

Test with:
```shell
docker compose up
```

Run with:
```shell
docker compose up -d
```
Go to: http://localhost:8080 *or the port you specified in docker-compose.yaml*
