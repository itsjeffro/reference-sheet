# Exec

## Import csv into table through docker

The following command would concatenate (cat) the file (source) from the host machine to a new file (destination) in the container.

```
docker exec -i [container] /bin/bash -c 'cat > source.csv' < destination.csv
```

## Import file to table

Enter mysql

```
mysql -u[user] -p [database]
```

```
LOAD DATA INFILE '/var/lib/mysql-files/[file]' INTO TABLE table_name FIELDS TERMINATED BY ',' LINES TERMINATED BY '\r\n' IGNORE 1 LINES;
```
