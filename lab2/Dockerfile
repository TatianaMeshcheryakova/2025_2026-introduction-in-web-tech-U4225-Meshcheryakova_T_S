
# 1. Использовать базовый образ python:3.9-slim (Требование 1)
FROM python:3.9-slim

# Установка системных пакетов и необходимых инструментов сборки:
# build-essential и python3-dev добавлены для устранения ошибок "exit code: 1"
# при установке зависимостей Flask в минималистичном образе.
RUN apt update && \
    apt install -y --no-install-recommends curl vim build-essential python3-dev && \
    rm -rf /var/lib/apt/lists/*

# 2. Установить рабочую директорию /app (Требование 2)
WORKDIR /app

# 3. Установить Python пакеты из файла requirements.txt
# (Предполагается, что requirements.txt содержит "Flask==3.0.x")
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# 4. Скопировать файл app.py в контейнер (Требование 4)
COPY app.py .

# 5. Создать пользователя appuser с UID 1000 (Требование 5)
RUN useradd -m -u 1000 appuser

# 6. Переключиться на пользователя appuser (Требование 6)
USER appuser

# 7. Открыть порт 5000 (Требование 7)
EXPOSE 5000

# 8. Установить переменную окружения FLASK_ENV=production (Требование 8)
ENV FLASK_ENV=production

# 9. Запустить приложение командой python app.py (Требование 9)
CMD ["python", "app.py"]
