# 1. Этап сборки
FROM golang:1.21 AS builder

# Устанавливаем рабочую директорию
WORKDIR /app

# Копируем исходный код
COPY main.go .

# Собираем бинарный файл
RUN go build -o app

# 2. Этап финального образа
FROM alpine:latest

# Устанавливаем рабочую директорию
WORKDIR /root/

# Копируем бинарник из первого контейнера
COPY --from=builder /app/app .

# Даем права на выполнение
RUN chmod +x app

# Запускаем приложение
CMD ["./app"]