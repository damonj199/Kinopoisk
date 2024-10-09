# Кинопоиск API

## Описание

Требуется реализовать WEB API для поиска фильмов по различным критериям и получения списка кинопремьер на текущий месяц.
Для доступа к API Кинопоиска необходимо зарегистрироваться на сайте и в разделе «профиль» получить API KEY.

## Требования

### База данных
Спроектировать БД PostgreSQL.

Необходимые поля:
- kinopoiskId;
- nameRu;
- posterUrl;
- countries;
- genres.

Синхронизировать БД с данными Кинопоиска.

### Эндпоинты и требования к ним

Создать эндпоинты на получение фильмов с возможностью
- Пагинации;
- Сортировки;
- Поиск фильмов по названию;
- Фильтрация по Countries и Genres (Можем выбрать один или несколько фильтров для получения фильмов).

Эндпоинты необходимо кэшировать в Redis с удалением по истечению 24 часов.

### Фоновые задачи

Создать scheduler(cron), который каждый месяц, 1 числа в 00:00 добавляет в БД список кинопремьер на текущий месяц и удаляет данные за предыдущий.

Приложение обернуть в Docker и создать docker-compose с проектом, БД и Redis.

### Технологии:
- C#;
- .NET;
- PostgreSQL;
- Docker;
- Redis.

### Ссылки:
- Kinopoisk API: https://kinopoiskapiunofficial.tech/
- Endpoint для получения кинопремьер: https://kinopoiskapiunofficial.tech/api/v2.2/filmes/premiers



