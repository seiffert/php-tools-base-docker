PHP-CLI-Tools Docker-Container
=========================

This repository creates a base-image for docker containers that run PHP command line tools.

Usage
--------------------

Use the `pseiffert/php-tools-base` container to create new PHP tools containers:

    ``` sh
    $ cat Dockerfile
    FROM pseiffert/php-tools-base

    RUN cd /opt/tools && composer require phploc/phploc

    ENTRYPOINT /opt/tools/bin/phploc