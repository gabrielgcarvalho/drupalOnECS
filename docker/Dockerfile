FROM drupal:9-php7.4-apache

WORKDIR /opt/drupal
RUN set -eux; \
    composer update symfony/var-dumper; \
    composer require drush/drush:^10; \
    composer update 
