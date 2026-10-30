# Архитектура

## Слои
- **controller** — REST-эндпоинты, валидация DTO, возврат DTO.
- **service** — бизнес-логика (загрузка работы, запуск проверки, расчёт уникальности).
- **repository** — Spring Data JPA.
- **entity** — сущности БД (Student, Teacher, Work, CheckResult, User).
- **dto** — объекты передачи данных с валидацией.
- **exception** — кастомные исключения и `@ControllerAdvice`.

## Основные сущности
- `User` (роль: STUDENT / TEACHER / ADMIN)
- `Work` (курсовая/дипломная работа: title, filePath, student, teacher, status)
- `CheckResult` (процент уникальности, список совпадений, дата проверки)

## Поток проверки
1. Студент загружает файл → `Work` в статусе `UPLOADED`.
2. Преподаватель/админ запускает проверку → `CheckResult` со статусом `IN_PROGRESS`.
3. По завершении — `CheckResult` с `uniquenessPercent` и ссылками на источники.
