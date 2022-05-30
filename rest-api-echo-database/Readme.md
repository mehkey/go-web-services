
## Go + Postgres

## Setup local database env

With docker we can setup a ephemeral postgres instance

```bash
docker run --name postgresql-container -p 5432:5432 -e POSTGRES_PASSWORD=password -e POSTGRES_USER=postgres -d postgres
```




To load the data using psql.



```bash
psql -h localhost -p 5432 -d postgres -f database/migration/000001_init.up.sql -U $(whoami)
```

```bash
go run cmd/web/main.go
```

```bash
curl localhost:7999/api/v1/users/1
```

