# docker-umami

Dockerized version of [umami](https://github.com/mikecao/umami).

## Use

### Bootstrap

```bash
git clone https://github.com/iferror/docker-umami && cd docker-umami
docker-compose pull
cp .env.placeholder .env
# edit .env
```

### Start server

```bash
docker-compose up -d
open http://localhost:3000
```

> Default password for the user `admin` is `umami` which is hardcoded in [there](https://github.com/mikecao/umami/blob/72065d0a0924977b78cdf4fba85775ae254bf960/sql/schema.postgresql.sql#L72). Change admin password as soon as you finish setting up.

### Stop server

```bash
docker-compose down
```

### Update server

```bash
docker-compose down --rmi local
git pull && docker-compose pull
docker-compose up -d
```
