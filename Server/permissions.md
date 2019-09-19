# Permissions

## Web permissions

### Web group

Add your user to the web server group.

```
$ sudo usermod -a -G www-data me
```

Note: log out and back in for the changes to take affect.

### Folder permissions

```
$ sudo chown -R me:www-data /var/www
```

Keep new files and directories within the "directory" having the same group permissions.

```
$ sudo chmod -R g+s /var/www
```

## Chmod

Folders: `755`
Files: `644`

```
find /var/www -type d -exec chmod 755 {} \;
```
```
find /var/www -type f -exec chmod 644 {} \;
```