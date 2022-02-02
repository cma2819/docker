FROM php:8.0-cli

# Composer
COPY --from=composer /usr/bin/composer /usr/bin/composer

RUN apt-get update && apt-get install -y git zip

CMD [ "composer", "run-script", "start" ]