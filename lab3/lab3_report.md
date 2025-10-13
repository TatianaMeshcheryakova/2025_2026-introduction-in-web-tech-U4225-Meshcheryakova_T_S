University: [ITMO University](https://itmo.ru/ru/)

Faculty: [FICT](https://fict.itmo.ru)

Course: [Введение в веб технологии](https://itmo-ict-faculty.github.io/introduction-in-web-tech/)

Year: 2025/2026

Group: U4225

Author: Meshcheryakova Tatiana Sergeevna

Lab: Lab3

Date of create: 10.10.2025

Date of finished: 13.10.2025

**Создание чистой папки**
Создана новая папка C:\DOCKER_MONITOR (без кириллицы) для обеспечения стабильного монтирования томов.
![](/lab3/32.png) 

**Создание конфигурации**
Создана подпапка PROMETHEUS_CONFIG
![](/lab3/33.png) 

**Создание metrics_config.yml**
Создан конфигурационный файл Prometheus, включающий цели для сбора метрик (Prometheus и Node Exporter).
![](/lab3/34.png) 

**Создание stack.yml**
Создан файл Docker Compose, описывающий все три сервиса. Критическое исправление: Исключение network_mode: host и использование относительного пути монтирования ./PROMETHEUS_CONFIG.
![](/lab3/35.png) 

**Запуск docker-compose**
Все контейнеры запущены командой docker-compose -f stack.yml up -d. Запуск прошел успешно.
![](/lab3/36.png) 

**Проверка docker ps**
Все три контейнера (Prometheus, Grafana, Node Exporter) находятся в статусе Up (работают).
![](/lab3/37.png) 

**Доступ к Prometheus**
Веб-интерфейс Prometheus успешно доступен по адресу http://localhost:9090.
![](/lab3/38.png) 

**Доступ к Grafana**
Веб-интерфейс Grafana успешно доступен по адресу http://localhost:3000.
![](/lab3/39.png) 

**Подключение источника данных (настройка)**
Настройка источника данных Prometheus с URL: http://prometheus:9090 (имя сервиса в Docker Compose).
![](/lab3/40.png) 

**Подключение источника данных (тест)**
Тест подключения успешен: "Successfully queried the Prometheus API."
![](/lab3/41.png) 

**Создание дашборда (Проблема с кавычками)**
Начало создания графика. Видна автоматическая замена двойных кавычек на одинарные (mode='idle'), что привело к ошибке синтаксиса
![](/lab3/42.png) 

**Создание дашборда**
После исправления синтаксиса (переходом в режим "Code" и использованием двойных кавычек) график появился. Визуализация переключена на вид Gauge (измеритель), показывающий текущую загрузку CPU (1.54%).
![](/lab3/44.png) 

**Сохранение дашборда**
Дашборд "Мониторинг Windows Server" успешно сохранен
![](/lab3/43.png) 
