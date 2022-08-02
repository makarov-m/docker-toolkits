Run Docker container with a database 
Db sample from https://www.postgresql.org/ftp/projects/pgFoundry/dbsamples/world/dbsamples-0.1/

1. create folder {path/folder_name}

2. create Dockerfile.txt in {path/folder_name}

FROM postgres
ENV POSTGRES_PASSWORD docker
ENV POSTGRES_DB world
COPY world.sql /docker-entrypoint-initdb.d/

3. put world.sql into folder {path/folder_name}

4. Launch commands in terminal

cd {path/folder_name}
docker build . -f Dockerfile.txt -t my-test-postgres-db
docker run -d --name my-postgres-container -p 5432:5432 my-test-postgres-db

5. connect to database

Host: localhost
Port: 5432
User: postgres
Password: docker







