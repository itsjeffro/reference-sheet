# Permissions

## Web permissions

```
$ sudo chown -R name:www-data directory
```

Keep new files and directories within "directory" having the same group permissions.

```
$ sudo chmod -R g+s directory
```

## Chmod

Folders: 755
Files: 644

```
find . -type d -exec chmod 755 {} \;
```
```
find . -type f -exec chmod 644 {} \;
```
