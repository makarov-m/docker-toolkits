# docker-toolkits

## 1. PostgreSQL 
**Description:** Run Docker container with a database inside. Database sample from [www.postgresql.org](https://www.postgresql.org/ftp/projects/pgFoundry/dbsamples/world/dbsamples-0.1/)

1. Clone repository 

2. Launch commands in terminal
```
cd {path/folder_name}
docker build . -f Dockerfile.txt -t my-test-postgres-db
docker run -d --name my-postgres-container -p 5432:5432 my-test-postgres-db
```
3. Connect to database using your database client

- Host: localhost
- Port: 5432
- User: postgres
- Password: postgres

4. Stop the container in terminal when you finish
```
docker stop my-postgres-container
```

