# Files

* inner.network -- Podman network containing communication between containers.
* mariadb.container -- Quadlet for MariaDB database, set up so it will run after
login or system boot, depending on user lingering.
* mariadb.env -- Setup base user and database for MariaDB.
* photoprism.container -- Quadlet for Photoprism, Volume with original images,
is set up to be read only -- this is is my backup of Digikam photos.
* photoprism.env -- Basic environment variables for Photoprism.

# Secrets
4 secrets in this setup.

* MYSQL_ROOT_PASSWORD -- password for root user of MariaDB.
* MYSQL_PASSWORD -- shared between MariaDB and Photoprism container.
* PHOTOPRISM_ADMIN_PASSWORD -- password to log into Photoprism instance
* PHOTOPRISM_SITE_URL -- Photoprism website URL.

# Other info

Skipping configuration for proxy server to host Photoprism. If not using proxy,
publish port by adding in photoprism.container
`PublishPort=<port_on_nas>:2342`. `port_on_nas` is port from which Photoprism
will be accessed.
