# postgres-stop
PostgreSQL Resource Center

### Introduction
The goal of this repository is to provide a resource center for learning PostgreSQL.

### Prerequisites
All of the work done here have been tested on Ubuntu 20.04 LTS and PostgreSQL 12.8.

### Installation
```
$ sudo apt-get update
$ sudo apt-get install postgresql postgresql-contrib
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
$ getent passwd | grep postgres
postgres:x:127:134:PostgreSQL administrator,,,:/var/lib/postgresql:/bin/bash
```

### Where is the data directory
```
$ sudo -i -u postgres
postgres@nuc2:~$ pwd
/var/lib/postgresql
postgres@nuc2:~$ cd 12/main
postgres@nuc2:~/12/main$ ls -AlF
total 84
drwx------ 5 postgres postgres 4096 Oct 31 15:00 base/
drwx------ 2 postgres postgres 4096 Oct 31 20:56 global/
drwx------ 2 postgres postgres 4096 Oct 31 15:00 pg_commit_ts/
drwx------ 2 postgres postgres 4096 Oct 31 15:00 pg_dynshmem/
drwx------ 4 postgres postgres 4096 Oct 31 20:13 pg_logical/
drwx------ 4 postgres postgres 4096 Oct 31 15:00 pg_multixact/
drwx------ 2 postgres postgres 4096 Oct 31 20:08 pg_notify/
drwx------ 2 postgres postgres 4096 Oct 31 15:00 pg_replslot/
drwx------ 2 postgres postgres 4096 Oct 31 15:00 pg_serial/
drwx------ 2 postgres postgres 4096 Oct 31 15:00 pg_snapshots/
drwx------ 2 postgres postgres 4096 Oct 31 20:08 pg_stat/
drwx------ 2 postgres postgres 4096 Oct 31 15:00 pg_stat_tmp/
drwx------ 2 postgres postgres 4096 Oct 31 15:00 pg_subtrans/
drwx------ 2 postgres postgres 4096 Oct 31 15:00 pg_tblspc/
drwx------ 2 postgres postgres 4096 Oct 31 15:00 pg_twophase/
-rw------- 1 postgres postgres    3 Oct 31 15:00 PG_VERSION
drwx------ 3 postgres postgres 4096 Oct 31 15:00 pg_wal/
drwx------ 2 postgres postgres 4096 Oct 31 15:00 pg_xact/
-rw------- 1 postgres postgres   88 Oct 31 15:00 postgresql.auto.conf
-rw------- 1 postgres postgres  130 Oct 31 20:08 postmaster.opts
-rw------- 1 postgres postgres  107 Oct 31 20:08 postmaster.pid
```

### References
- [PostgreSQL Home](https://www.postgresql.org/)
- [How To Install PostgreSQL on Ubuntu 20.04](https://www.digitalocean.com/community/tutorials/how-to-install-postgresql-on-ubuntu-20-04-quickstart)
- [PostgreSQL Tutorial](https://www.postgresqltutorial.com/)
- [Node.js Postgresql tutorial: Build a simple REST API with Express step-by-step](https://geshan.com.np/blog/2021/01/nodejs-postgresql-tutorial/)
