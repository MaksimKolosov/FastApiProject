# Создать том:
docker volume create shorturl_data

# Собрать образ:
docker build -t short_url:latest .

# Запустить сервис:
docker run -d -p 8001:80 -v shorturl_data:/app/data short_url:latest

# Открыть сервис в браузере для удобного тестирования:
http://localhost:8001/docs