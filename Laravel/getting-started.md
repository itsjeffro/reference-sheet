# Getting started

## Permissions
When deploying to a server, permissions will need to be set. Which will allow for certain files or directories to be created by certain users and/or groups.

```bash
sudo chgrp -R www-data storage bootstrap/cache 

sudo chmod -R ug+rwx storage bootstrap/cache
```
