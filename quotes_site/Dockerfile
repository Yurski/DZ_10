# Dockerfile
FROM python:3.11

# Встановлюємо робочу директорію
WORKDIR /app

# Копіюємо файли
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt
COPY . .

# Виставляємо порт
EXPOSE 8000

# Команда для запуску сервера
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "quotes_site.wsgi:application"]
