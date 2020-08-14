# PHP

## PHP Unit

Assuming that you have phpunit installed using `composer` you maybe use the available Docker PHP image.

```bash
docker run -it --rm --name phpunit -v $PWD:/app -w /app php:7.4-cli php vendor/phpunit/phpunit/phpunit
```

This will do the following:

1. `-v $PWD:/app` will set the current directory you're inside the the container within an `app` directory.
2. `-w /app` will set the container's directory as the working directory.
3. `php:7.4-cli` will be the docker image we'll use.
4. `php vendor/phpunit/phpunit/phpunit` will be the command to run inside the contaier.
