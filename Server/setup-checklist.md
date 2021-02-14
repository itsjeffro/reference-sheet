# Set up checklist

## Add user

Add a new user.

```bash
sudo adduser jeff
```

Add the user to the `sudo` group.
```bash
sudo usermod -aG sudo jeff
````

### Setup SSH

```bash
su jeff
```

```bash
mkdir ~/.ssh && touch ~/.ssh/authorized_keys
```

## Certbot

```bash
sudo aptget install certbot
```

If nginx is being used then install the required plugin.

```bash
sudo apt-get install python3-certbot-nginx
```
