FROM mysql:latest
LABEL name="Studentapp"
ENV MYSQL_ROOT_PASSWORD = 12345
COPY database.sql /docker-entrypoint-database.sql
CMD [ "mysqld" ]