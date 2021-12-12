FROM drupal:9-php7.4-apache


# Install Drush
RUN useradd -u 8877 nonroot
RUN chown -R nonroot /opt/drupal
RUN chmod 755 /opt/drupal
WORKDIR "/opt/drupal"
USER nonroot
RUN pwd
RUN composer update global symfony/var-dumper
RUN composer require global drush/drush:^10 && \
    composer global update
