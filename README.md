# Import Sql File into DB:

Locate the PostgreSQL Container:
```
sudo docker ps
```

Copy the SQL File into the Container:
```
sudo docker cp /path/to/file_name.sql <container_name>:/file_name.sql
```

Import SQL File Using psql:
```
sudo docker exec -it <container_name> bash
```
```
psql -U <username> -d <database_name> -f /file_name.sql
```


# Export sql File into DB:
```
sudo docker exec -i <container_name> psql -U <username> -d <database_name> < /path/to/file_name.sql
```


# Base Docker Commands:

Build Docker:
```
sudo docker compose -p project_name -f docker_file_path.yml build
```

Up docker server:
```
sudo docker compose -p project_name -f docker_file_path.yml up -d
```

Down docker server:
```
sudo docker compose -p project_name down
```

Show docker containers:
```
sudo docker ps
```

Show docker all containers:
```
sudo docker ps -a
```

Restart docker container:
```
sudo docker compose -p project_name restart
```



# Install WiFi Driver

Run the commands
```
sudo apt update
```
```
sudo apt install dkms
```
```
git clone https://github.com/aircrack-ng/rtl8812au.git
```
```
cd rtl8812au
```
```
sudo make dkms_install
```

Load the Driver
```
sudo modprobe 8812au
```

Check if WiFi is working
```
iwconfig
```
         OR 
```
nmcli device
```





