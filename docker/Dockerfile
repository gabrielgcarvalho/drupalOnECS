FROM drupal:9-php7.4-apache


# Install Drush
RUN useradd -u 8877 nonroot && chown -R nonroot /opt/drupal && chmod 755 /opt/drupal
WORKDIR "/opt/drupal"
USER nonroot
RUN composer update symfony/var-dumper && composer require drush/drush:^10 && composer update
USER root
CMD sed -i "s/80/80/g" /etc/apache2/sites-enabled/000-default.conf /etc/apache2/ports.conf
