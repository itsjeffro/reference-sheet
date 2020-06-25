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

```bash
There are 4 choices for the alternative editor (providing /usr/bin/editor).

  Selection    Path                Priority   Status
------------------------------------------------------------
  0            /bin/nano            40        auto mode
  1            /bin/ed             -100       manual mode
  2            /bin/nano            40        manual mode
* 3            /usr/bin/vim.basic   30        manual mode
  4            /usr/bin/vim.tiny    15        manual mode

Press <enter> to keep the current choice[*], or type selection number:
```

Restarting php service without the root password prompt.

```bash
sudo visudo -f /etc/sudoers.d/{filename}
```

Then add ...

```bash
user ALL=NOPASSWD: /usr/sbin/service php7.0-fpm reload`
```
