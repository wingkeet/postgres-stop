# postgres-stop
PostgreSQL Resource Center

### Introduction
The goal of this repository is to provide a resource center for learning PostgreSQL.

### Prerequisites
All of the work done here have been tested on Ubuntu 20.04 LTS and PostgreSQL 12.8.

### Installation
```
$ sudo apt-get update
$ sudo apt-get install -y postgresql postgresql-contrib
```

### Get into the psql interactive shell
```
$ sudo -u postgres psql
psql (12.8 (Ubuntu 12.8-0ubuntu0.20.04.1))
Type "help" for help.

postgres=# \c
You are now connected to database "postgres" as user "postgres".
postgres=# \conninfo
You are connected to database "postgres" as user "postgres" via socket in "/var/run/postgresql" at port "5432".
```

### Home directory of the postgres user
```
$ getent passwd postgres
postgres:x:127:134:PostgreSQL administrator,,,:/var/lib/postgresql:/bin/bash
```

### Where are the PostgreSQL files?

| Location                      | Description         |
| ----------------------------- | ------------------- |
| `/etc/postgresql/12/main`     | Configuration files |
| `/var/lib/postgresql/12/main` | Data directory      |
| `/var/log/postgresql`         | Log files           |

### References
- [PostgreSQL Home](https://www.postgresql.org/)
- [How To Install PostgreSQL on Ubuntu 20.04](https://www.digitalocean.com/community/tutorials/how-to-install-postgresql-on-ubuntu-20-04-quickstart)
- [PostgreSQL Tutorial](https://www.postgresqltutorial.com/)
- [Node.js Postgresql tutorial: Build a simple REST API with Express step-by-step](https://geshan.com.np/blog/2021/01/nodejs-postgresql-tutorial/)
