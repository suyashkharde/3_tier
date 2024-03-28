FROM mysql
LABEL name="Studentapp"
ENV MYSQL_ROOT_PASSWORD=12345
COPY init-db.sql /docker-entrypoint-initdb.d/
CMD [ "mysqld" ]