# Создать том:
docker volume create todo_data

# Собрать образ:
docker build -t todo-sqlite:latest .

# Запустить сервис:
docker run -d -p 8000:80 -v todo_data:/app/data todo-sqlite:latest

# Открыть сервис в браузере для удобного тестирования:
http://localhost:8000/docs