University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Введение в веб технологии](https://itmo-ict-faculty.github.io/introduction-in-web-tech/)
Year: 2025/2026
Group: U4225
Author: Meshcheryakova Tatiana Sergeevna
Lab: Lab1
Date of create: 07.10.2025
Date of finished: 10.10.2025

| **Установка Docker Desktop (Работает)** | | ![](/lab1/1.png) |
| **Проверка версии** | `docker --version` | ![](/lab1/2.png) |
| **Тестовый запуск** | `docker run hello-world` | ![](/lab1/3.png) |
| **Проверка образов** | `docker images` | ![](/lab1/4.png) |
| **Проверка контейнеров** | `docker ps` и `docker ps -a` | ![](/lab1/5.png) |

| **Скачать образ** | `docker pull ubuntu:latest` | ![](/lab1/6.png) |
| **Запустить контейнер** | `docker run -it ubuntu bash` | ![](/lab1/7.png) |
| **Установка пакета** | `apt update && apt install -y curl` | ![](/lab1/8.png) |
| **Проверка установки и выход** | `curl --version` и `exit` | ![](/lab1/9.png) |

| **Проверка в браузере** | `http://localhost:8080` | ![](/lab1/10.png) |
| **Просмотр логов,подключение к контейнеру** | `docker logs web-server` | ![](/lab1/11.png) |

| **Остановка и запуск (1)** | `docker ps`, `docker stop`, `docker start` | ![](/lab1/12.png) |
| **Остановка и запуск (2)** | `docker stop`, `docker start` (Продолжение) | ![](/lab1/13.jpg) |
| **Удаление контейнера и образа** | `docker stop`, `docker rm web-server`, `docker rmi nginx:alpine` | ![](/lab1/14.jpg) |

| **Создание тома и файла** | `docker volume create my-volume` и создание файла | ![](/lab1/15.png) |
| **Проверка сохранения** | Удаление старого контейнера и проверка файла в новом | ![](/lab1/16.jpg) |
