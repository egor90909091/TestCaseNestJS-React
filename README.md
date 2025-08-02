# Проект: Backend на NestJS и Frontend на React

## Описание
Это проект с backend на NestJS и frontend на React.  
Backend работает на порту **5001**, frontend — на порту **3000**.

## Backend (NestJS)
- Сервер работает на порту `5001`.
- В репозитории находится файл `.env` с конфигурацией для Postgres и JWT token (понимаю, что не лучшая практика .env передавать).
- В корне backend репозитория есть `docker-compose.yml`, с помощью которого можно запустить Postgres 15 на  порт 5432.
- Лучше было бы вынести `docker-compose.yml` в корень всего проекта, но сейчас он лежит внутри backend.

## Frontend (React)
- Приложение работает на порту `3000`.


## Запуск проекта

### Запуск backend с Docker Compose
```bash

cd backend
docker compose up dev-db -d
npx prisma migrate deploy
npm run start:dev               

cd frontend
npm start
