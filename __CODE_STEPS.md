## Setup Project
1. Clone Git Repository in project folder
```
$ git clone git@github.com:username/repository_name.git .
```

2. Copy __.env.docker__ file to __.env__ and edit database credentials there
```
$ cp .env.docker .env
```

3. Install application composer dependencies via Docker
```
$ docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v $(pwd):/var/www/html \
    -w /var/www/html \
    laravelsail/php81-composer:latest \
    composer install --ignore-platform-reqs
```

4. Start application via docker
```
$ ./vendor/bin/sail up
```

5. Run migrations & seed data
```
$ ./vendor/bin/sail artisan migrate --seed
```

--------------------------------------------------------------------------------

6. Create vue js application
```
$ ./vendor/bin/sail npm init vite vue
$ vue
$ vue
```

7. Run npm from vue folder (__npm i__ installs a package and all its dependencies.)
```
$ cd vue
$ .././vendor/bin/sail npm i
$ .././vendor/bin/sail npm run dev
```
