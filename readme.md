# PostgreSQL Docker

[**DockerHub Repository Link**](https://hub.docker.com/r/registryhj/postgres)

<br />

## Supported Tags

- [`17.2`](https://hub.docker.com/layers/registryhj/postgres/17.2/images/sha256-c2e9766b2a69a5a13185d4fc57b62eac251ed31395e5ce17ee876f17045ece5e)
- [`16.6`](https://hub.docker.com/layers/registryhj/postgres/16.6/images/sha256-f4361ce5744858148d603d045710db4e79b6e00b1d12d9118677172b1d6f458d)
- [`15.10`](https://hub.docker.com/layers/registryhj/postgres/15.10/images/sha256-e9b9d8b6e2011fa716de77be5333ad3c2e035166d7424459b661aa978121d849)
- [`14.15`](https://hub.docker.com/layers/registryhj/postgres/14.15/images/sha256-cbc5ba1521e947f7c5633c8590f08de50dfcf40a537bd7159b7fedab54a5352b)
- [`13.18`](https://hub.docker.com/layers/registryhj/postgres/13.18/images/sha256-4dae7b3e714035b916ad1139470de7f3f329f215361ec4f0444e485c11cd64f5)

<br />

## How to use

**Pull this image:**

```
docker pull registryhj/postgres:<tag_name>
```

**Create container in background process:**

```
docker run \
    --name <container_name> \
    -p <port>:5432 \
    -e POSTGRES_PASSWORD=<password> \
    registryhj/postgres:<tag_name>
```

or (if you want to set `User`):

```
docker run \
    --name <container_name> \
    -p <port>:5432 \
    -e POSTGRES_USER=<user> \
    -e POSTGRES_PASSWORD=<password> \
    registryhj/postgres:<tag_name>
```

or (if you want to set `Database`):

```
docker run \
    --name <container_name> \
    -p <port>:5432 \
    -e POSTGRES_USER=<user> \
    -e POSTGRES_PASSWORD=<password> \
    -e POSTGRES_DB=<database> \
    registryhj/postgres:<tag_name>
```

**Execute Shell Prompt:**

```
docker exec -it <container_name> zsh
```

**Execute PSQL Prompt:**

```
docker exec -it <container_name> psql -U postgres
```

or (if you set `--env POSTGRES_USER=<user>`):

```
docker exec -it <container_name> psql -U <user>
```

or (if you set `--env POSTGRES_DATABASE=<database>`)

```
docker exec -it <container_name> psql -U <user> -d <database>
```

<br />

## Supported Architectures

- `linux/amd64`
- `linux/arm64`

# <br />

Copyright © 2025 RegistryHJ
