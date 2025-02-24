FROM nginx:latest

# Копируем кастомный конфиг
COPY nginx.conf /etc/nginx/nginx.conf

# Создаем директорию для логов (если нужно)
RUN mkdir -p /var/log/nginx

# Открываем порты
EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]