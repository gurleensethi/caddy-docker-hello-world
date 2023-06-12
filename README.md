# caddy-docker-hello-world

Running using docker:

```bash
docker run --rm --name caddy -p 8080:80 -v ${PWD}/Caddyfile:/etc/caddy/Caddyfile caddy:latest
```

With Compose:

```yaml
version: '3.8'

services:
  caddy:
    image: caddy:latest
    ports:
      - 8080:80
    volumes:
      - ${PWD}/Caddyfile:/etc/caddy/Caddyfile
```

```bash
docker compose up
```
