# Configuring HTTPS servers

## Reusable snippet
To minimise bloat in the nginx site config, a snippet can be created and inlcuded in the server conf for ssl related contents, such as ciphers.

This allows for:
* Reusability
* Less cognitive load

1. Create a file path if it does not exist already.

```
$ sudo touch /etc/nginx/snippets/ssl.conf
```

2. To determine the contents of ssl.conf, use Mozillas SSL generator, https://mozilla.github.io/server-side-tls/ssl-config-generator/

Server Version
```
$ nginx -v
```

OpenSSL Version
```
$ openssl version
```

3. Copy the generated contents (ciphers etc) to ssl.conf and save.

## Server block
1. Open up your sites nginx conf in /etc/nginx/sites-available/

2. Add new blocks which will handle redirecting normal http requests to https.

```
// Redirects http to https
server {
  listen 80;

  server_name example.com www.example.com;
  
  return 301 https://$server_name$request_url;
}

// Redirects https with www to https non-www
server {
  listen 443 ssl;
  
  server_name www.example.com;

  ssl_certificate /path/to/fullchain.pem;
  ssl_certificate_key /path/to/privkey.pem;
  ssl_certificate_certificate /path/to/chain.pem;
  
  include /etc/nginx/snippets/ssl.conf;
  
  return 301 https://example.com$request_url;
}
```

3. Update the original port 80 to listen for 443.

```
server {
  # listen 80;
  listen 443 ssl;

  # ...
```

4. Add the paths to the ssl pems with the original server block as well after you have changed the port from 80 to 443.

```
  # ...

  ssl_certificate /path/to/fullchain.pem;
  ssl_certificate_key /path/to/privkey.pem;
  ssl_certificate_certificate /path/to/chain.pem;
  
  include /etc/nginx/snippets/ssl.conf;
  
  # ...
```