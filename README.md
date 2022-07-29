# Fastapi-Postgres-Docker

Postgres, FastAPI, and Docker

--Create postgres image on docker
docker pull postgres:alpine

docker images

docker run --name fastapi-postgres -e POSTGRES_PASSWORD=[password] -d -p 5432:5432 postgres:alpine

docker ps

docker exec -it fastapi-postgres bash

psql -U postgres

create database fastapi_database;

 create user myuser with encrypted password '[password]';

 grant all privileges on database fastapi_database to myuser;

 \c fastapi_database;

--make database available outside container
  psql -h localhost -p 5432 postgres

  py -m venv venv
  venv/scripts/activate

  pip install fastapi[all]
  pip install SQLAlchemy psycopg2-binary


  --add table to database
  python
  import services
  services._create_database()

  pgadmin

--list all tables
  \dt 
