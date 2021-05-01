FROM mysql:5.6

COPY ./sql-scripts/ /docker-entrypoint-initdb.d/

ENV MYSQL_DATABASE products
ENV MYSQL_ROOT_PASSWORD password
ENV MYSQL_USER root

EXPOSE 3306