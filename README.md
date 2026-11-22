## Шаблон для третьего ДЗ по ИПР

Условие дз доступно по [ссылке](https://github.com/Nikfilk2030/missing_semester_hse_cs/blob/main/2026/amcs/year_1/hw_3/README.md)

# Docker Homework

## 6 баллов SQLite
`app` запускается через Docker Compose.\
`DATA_FILE=/data/counter.db` - путь к базе SQLite.\
`data_counter:/data` - том для сохранения данных.\
Запуск - `docker compose up -d --build`\
Проверка - `docker compose ps`\
Остановка - `docker compose down`
## 8 баллов Redis
Два сервиса: `app` и `redis`.\
`STORAGE=redis` - использование Redis.\
`REDIS_URL=redis://redis:6379/0` - адрес Redis.\
`data_redis:/data` - том для сохранения данных Redis.\
Запуск: `docker compose up -d --build`\
Проверка логов: `docker compose logs`\
Остановка: `docker compose down` (данные остаются).\
Redis: `docker compose stop redis` / `docker compose start redis`.\
Использовать `docker compose down -v`, если нужно удалить данные.

## Все логи лежат в /answers