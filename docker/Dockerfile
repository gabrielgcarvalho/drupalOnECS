FROM drupal:9-php7.4-apache

RUN set  -eux; \
    apt-get update; \
    apt-get install -y --no-install-recommends git
CMD /bin/sh -c "drush en -y admin_toolbar admin_toolbar_tools"