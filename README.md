# Import Sql File into DB:

Locate the PostgreSQL Container:
```
sudo docker ps
```

Copy the SQL File into the Container:
```
sudo docker cp /path/to/jan21_dev_db.sql <container_name>:/file_name.sql
```

Import SQL File Using psql:
```
sudo docker exec -it <container_name> bash
```
```
psql -U <username> -d <database_name> -f /jan21_dev_db.sql
```


# Export sql File into DB:
```
docker exec -i <container_name> psql -U <username> -d <database_name> < /path/to/file_name.sql
```
