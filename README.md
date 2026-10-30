# Plagiarism Check Service

## Концепция
Сервис учёта и проверки курсовых/дипломных работ на антиплагиат. Позволяет:
- загружать работы (PDF/DOCX) и хранить метаданные;
- запускать проверку уникальности (внутренняя база + внешние источники);
- формировать отчёты (процент уникальности, совпадения, ссылки на источники);
- вести учёт по студентам, дисциплинам и преподавателям;
- разграничивать роли: студент, преподаватель, администратор.

## Технологический стек
| Слой | Технология |
|---|---|
| Язык | Java 17 |
| Backend | Spring Boot 3 |
| База данных | PostgreSQL 16 |
| ORM | Spring Data JPA / Hibernate |
| Миграции | Flyway |
| Безопасность | Spring Security + JWT |
| Документация API | Swagger / OpenAPI |
| Тесты | JUnit 5, Mockito, Spring Boot Test |
| Контейнеризация | Docker + docker-compose |
| CI | GitHub Actions |

## Развертывание
1. Клонировать репозиторий:
   ```bash
   git clone https://github.com/<ваш-аккаунт>/plagiarism-check-service.git
   cd plagiarism-check-service
