# PHP Service

## PHP service

```
sudo pkill php5-fpm

sudo service php5-fpm start
```

## OPcache and Symlinks

Restarting php service without the root password prompt.

```bash
sudo visudo -f /etc/sudoers.d/{filename}
```

Then add ...

`user ALL=NOPASSWD: /usr/sbin/service php7.0-fpm reload`
