# a lightweight linux distribution
FROM tomcat:8.0-alpine

WORKDIR /app
COPY ./java-app.jar /app

# Порт, который "прослушивается" дистрибутивом tomcat внутри контейнера
EXPOSE 8080

# Запуск дистрибутива tomcat
CMD ["catalina.sh", "run"]

# Периодечкая проверка работоспособности контейнера путём запросов по указанному URL. Если запрос не пройдёт, то контейнер должен завершить свою работу
HEALTHCHECK CMD curl --fail http://localhost:80/webapi/ || exit 1
