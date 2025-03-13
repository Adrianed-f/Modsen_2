# Используем официальный образ Nginx
FROM nginx:latest

# Удаляем стандартную страницу Nginx и заменяем своей
COPY index.html /usr/share/nginx/html/index.html

# Открываем порт 80 для контейнера
EXPOSE 80