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