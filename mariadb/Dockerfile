# Dockerfile
# syntax=docker/dockerfile:1

# Dockerfile
FROM mariadb


ENV MARIADB_ROOT_PASSWORD=root
ENV MARIADB_USER=ead_user
ENV MARIADB_PASSWORD=ead_password
ENV MARIADB_DATABASE=ead_joomla

COPY ./db/ /docker-entrypoint-initdb.d/


