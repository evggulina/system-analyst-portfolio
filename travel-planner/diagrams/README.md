# Диаграммы проекта TravelTech

В этой папке находятся все диаграммы, созданные в ходе работы.  
Файлы представлены в двух форматах: .drawio / .puml (исходники) и .png (для быстрого просмотра).

| Имя файла | Тип диаграммы | Описание |
|-----------|---------------|----------|
| [use-case.drawio](use-case.drawio) / [use-case.png](use-case.png) | Use Case | Показывает акторов (Пользователь, Организатор, Участник, Внешние API) и их взаимодействие с системой. Основные сценарии: создание поездки, добавление рейса/отеля/активности, управление участниками, обработка конфликтов, интеграция с внешними API. |
| [activity-diagram.drawio](activity-diagram.drawio) / [activity-diagram.png](activity-diagram.png) | Activity | Детализирует процесс разрешения конфликтов: обнаружение, уведомление, предложение вариантов, голосование (с весом голосов), применение решения. |
| [01-flight-search.puml](01-flight-search.puml) / [01-flight-search.png](01-flight-search.png) | Sequence (поиск рейса) | Взаимодействие при поиске рейсов: сначала опрашивается СИРЕНА, при ошибке выполняется fallback на Яндекс.Авиа. Возвращается список рейсов с полем `provider`. |
| [02-flight-selection-passengers.puml](02-flight-selection-passengers.puml) / [02-flight-selection-passengers.png](02-flight-selection-passengers.png) | Sequence (выбор рейса и пассажиры) | Детали выбранного рейса запрашиваются у того же провайдера; затем вводятся данные пассажиров, провайдер сохраняется в БД. |
| [03-payment-booking.puml](03-payment-booking.puml) / [03-payment-booking.png](03-payment-booking.png) | Sequence (оплата и бронирование) | Обработка платежа через платёжный шлюз, получение webhook (успех/ошибка), финальное бронирование у провайдера и уведомление пользователя. |
| [er-diagram.drawio](er-diagram.drawio) / [er-diagram.png](er-diagram.png) | ER (сущность-связь) | Логическая модель данных: таблицы users, trips, trip_participants, child_passengers, flight_bookings, hotel_bookings, activity_bookings, booking_participants, child_booking_links; показаны ключи, типы данных, ограничения NOT NULL и связи. |

## 🔧 Инструменты
- Исходники .drawio открываются в [draw.io](https://app.diagrams.net/).
- Для просмотра .png достаточно любого браузера или программы для просмотра изображений.
- .puml — текстовое описание диаграмм (PlantUML), можно открыть в любом текстовом редакторе или сгенерировать изображение через [PlantUML сервер](https://www.plantuml.com/plantuml/uml/).

## 📬 Контакты
Если есть вопросы по диаграммам, пишите: [evg_gulina@mail.ru](mailto:evg_gulina@mail.ru) или Telegram [@GulinaEvg](https://t.me/GulinaEvg)
