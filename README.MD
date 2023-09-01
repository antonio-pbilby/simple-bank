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