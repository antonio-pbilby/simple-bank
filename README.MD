# Go Project from Udemy

[Course Link](https://www.udemy.com/course/backend-master-class-golang-postgresql-kubernetes/)

### To run migrations with GO

Install [golang-migrate](https://github.com/golang-migrate/migrate)

```shell
brew install golang-migrate
```

```shell
migrate -path db/migration -database "postgresql://root:secret@localhost:5432/simplebank?sslmode=disable" -verbose up
```

### Using SQLC

Install

```shell
brew install sqlc
#or
sudo snap install sqlc
```

Init
```
sqlc init
```

Configure yaml
```yaml
version: "2"
sql:
  - engine: "postgresql" 
    queries: "./db/query" #folder to queries
    schema: "./db/migration" #folder to schemas or in this case migrations
    gen:
      go:
        package: "db" #package name
        out: "./db/sqlc" #output folder
```