FROM mysql:5.7.18

ENV MYSQL_DATABASE=sqlpractice \
    MYSQL_ROOT_PASSWORD=localpassword

ADD ./data/lahman2016.sql /docker-entrypoint-initdb.d

EXPOSE 3306