# Дорожная карта проекта Messenger

## **Этап 1: Основной MVP (Завершено)**

### Реализованные функции:

1. **Аутентификация и авторизация:**

   * Аутентификация на основе JWT.
   * Регистрация и вход пользователей.
2. **Базовая система сообщений:**

   * Отправка сообщений в реальном времени с помощью SignalR.
   * Сохранение сообщений в PostgreSQL.
3. **Интеграция с базой данных:**

   * Entity Framework Core с PostgreSQL.
4. **Архитектура бэкенда:**

   * Простая монолитная архитектура.
5. **Развёртывание:**

   * Докеризация приложения с использованием Docker Compose.
   * Настроенный volume для базы данных.

## **Этап 2: Обратная связь и исправление ошибок**

### Цели:

1. Получение обратной связи от фронтенд-разработчика.
2. Исправление выявленных багов и недочётов в MVP.
3. Оптимизация SignalR для повышения производительности в реальном времени.
4. Улучшение системы логирования и отладки.

---

## **Этап 3: Улучшения и добавление функционала**

### Запланированные функции:

1. **Поддержка файлов и изображений:**

   * Реализация функционала загрузки файлов.
   * Хранение файлов и изображений в облачном хранилище (S3).
   * Добавление проверки размера и типа файлов.

2. **Функция поиска:**

   * Возможность поиска по сообщениям и пользователям.
   * Поддержка полнотекстового поиска в PostgreSQL.

3. **Групповые чаты:**

   * Реализация функционала групповых чатов.
   * Создание API для управления группами (создание, добавление/удаление пользователей).

4. **Профили пользователей:**

   * Управление профилями пользователей (например, аватар, биография).
   * Просмотр профилей других пользователей.

5. **Кэширование с использованием Redis:**

   * Кэширование профилей пользователей и данных аутентификации.
   * Хранение временных данных сообщений для оптимизации производительности.

---

## **Этап 4: Масштабирование архитектуры**

### Цели:

1. **Переход на микросервисы:**

   * Разделение бэкенда на отдельные сервисы (например, аутентификация, чат, файловое хранилище).
   * Использование RabbitMQ для коммуникации между сервисами.
   * Введение API Gateway для маршрутизации запросов.

2. **Оптимизация WebSocket:**

   * Переход с SignalR на чистый WebSocket для уменьшения нагрузки.
   * Реализация балансировки нагрузки для подключений WebSocket.

3. **Масштабирование базы данных:**

   * Переход с PostgreSQL на Citus для поддержки распределённой базы данных.
   * Реализация шардирования для обеспечения высокой масштабируемости.

4. **Улучшение безопасности:**

   * Введение двухфакторной аутентификации.
   * Ограничение частоты запросов для предотвращения злоупотреблений.
   * Сканирование загружаемых файлов на наличие вредоносных программ.

---

## **Этап 5: Расширенные функции**

### Цели:

1. **Push-уведомления:**

   * Интеграция push-уведомлений для обновлений в реальном времени.
2. **Аналитическая панель:**

   * Создание панели для мониторинга метрик использования и производительности.
3. **Оптимизация поиска:**

   * Реализация продвинутого поиска с фильтрами (например, диапазон дат, тип сообщений).
4. **Локализация:**

   * Поддержка нескольких языков.

---

## **Этап 6: Финализация и улучшение**

### Цели:

1. **Рефакторинг кода:**

   * Повышение читаемости и поддерживаемости кода.
2. **Тестирование:**

   * Написание юнит-тестов, интеграционных тестов и тестов производительности.
3. **Документация:**

   * Создание подробной документации по API и архитектуре системы.
4. **Развёртывание в продакшн:**

   * Подготовка инфраструктуры для работы в режиме реального времени.

---

## Заметки:

* После каждого этапа будет проводиться ретроспектива для оценки прогресса и корректировки планов.

**Текущий фокус:** Ожидание обратной связи от фронтенда и подготовка к улучшениям на этапе 3.
