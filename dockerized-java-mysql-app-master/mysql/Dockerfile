# Используем офф. образ mysql
FROM mysql
# Добавляем базу данных
ENV MYSQL_DATABASE company
# Добавляем всё из директории sql-scripts/ в образ
# Все скрипты в docker-entrypoint-initdb.d/ будут автоматически выполнены при старте docker-compose
COPY ./sql-scripts/ /docker-entrypoint-initdb.d/
