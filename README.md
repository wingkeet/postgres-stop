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

### Home directory of the postgres user
```
$ getent passwd postgres
postgres:x:127:134:PostgreSQL administrator,,,:/var/lib/postgresql:/bin/bash
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

### Where are the PostgreSQL files?
```
postgres=# SELECT name, setting FROM pg_settings WHERE category = 'File Locations';
       name        |                 setting                 
-------------------+-----------------------------------------
 config_file       | /etc/postgresql/12/main/postgresql.conf
 data_directory    | /var/lib/postgresql/12/main
 external_pid_file | /var/run/postgresql/12-main.pid
 hba_file          | /etc/postgresql/12/main/pg_hba.conf
 ident_file        | /etc/postgresql/12/main/pg_ident.conf
(5 rows)
```
The following are the default file locations on Debian or Ubuntu systems:

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
