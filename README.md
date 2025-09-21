### Стек технологий:

[![FastAPI](https://img.shields.io/badge/-FastAPI-464646?style=flat-square&logo=FastAPI)](https://fastapi.tiangolo.com/)
[![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-464646?style=flat-square&logo=PostgreSQL)](https://www.postgresql.org)
[![SQLAlchemy](https://img.shields.io/badge/-SQLAlchemy-464646?style=flat-square&logo=SQLAlchemy)](https://www.sqlalchemy.org/)
[![docker](https://img.shields.io/badge/-Docker-464646?style=flat-square&logo=docker)](https://www.docker.com)


### Описание проекта 
API-сервис для управления вопросами и ответами.

Сервис позволяет:

- Создавать вопросы.
- Отвечать на вопросы.
- Получать список всех вопросов.
- Получать вопрос с ответами.
- Удалять вопросы и ответы (каскадно).

Логика:

-Нельзя создать ответ к несуществующему вопросу.
-Один и тот же пользователь может оставлять несколько ответов на один вопрос.
-При удалении вопроса должны удаляться все его ответы (каскадно).


###  Запуск проекта через Docker

### 1. Склонировать репозиторий:

```bash
git clone https://github.com/studalbert/TestTaskFastAPI.git
```
```bash
cd TestTaskFastAPI
```
### 2. Файл .env
```bash
Создать .env файл с настройками базы данных по образцу .env.template
```
### 3. Запустить контейнеры в фоне
```bash
docker compose up -d
```

Swagger документация доступна по адресу: http://localhost:8000/docs

### API Endpoints
### Вопросы (Questions)

| Метод | URL | Описание |
|-------|-----|----------|
| GET   | /questions/ | Получить список всех вопросов |
| POST  | /questions/ | Создать новый вопрос |
| GET   | /questions/{id} | Получить вопрос и все ответы на него |
| DELETE| /questions/{id} | Удалить вопрос (вместе с ответами) |

### Ответы (Answers)

| Метод | URL | Описание |
|-------|-----|----------|
| POST  | /questions/{id}/answers/ | Добавить ответ к вопросу |
| GET   | /answers/{id} | Получить конкретный ответ |
| DELETE| /answers/{id} | Удалить ответ |


### Автор работы

Алексей Ужва

VK: [@uzhvaaa](https://vk.com/uzhvaaa)
