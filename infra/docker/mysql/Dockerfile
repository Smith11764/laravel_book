FROM mysql/mysql-server:8.0

ENV TZ=Asia/Tokyo

COPY ./infra/docker/mysql/my.cnf /etc/my.cnf

RUN { \
    echo "ALTER USER 'root'@'%' IDENTIFIED WITH mysql_native_password BY 'root';"; \
    } > ./docker-entrypoint-initdb.d/user_init.sql
