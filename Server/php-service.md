# PHP Service

## PHP service

```
sudo pkill php5-fpm

sudo service php5-fpm start
```

## OPcache and Symlinks

(optional) Set the editor to use

```bash
sudo update-alternatives --config editor
```

This will display a list of options to choose from, such as `vim.basic`.

Restarting php service without the root password prompt.

```bash
sudo visudo -f /etc/sudoers.d/{filename}
```

Then add ...

`user ALL=NOPASSWD: /usr/sbin/service php7.0-fpm reload`
