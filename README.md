# Procrastinate_Pro

# Маркетинговый анализ Procrastinate Pro+

**Цель:** Выявить причины почему последние несколько прошлых месяцев наш бизнес постоянно нес убытки, хотя в привлечение пользователей была вложена куча денег.

**Задачи:** 
- Выявить проблемы и ошибки в маркетинговой политке компании.
- Подготовить список рекомендаций для маркетологов.

**Данные:** лог сервера с данными о посещениях приложения новыми пользователями, зарегистрировавшимися в период с 2019-05-01 по 2019-10-27, выгрузка их покупок за этот период, а также статистика рекламных расходов. 

**Шаги:**

- Шаг 1. Загрузка данных и подготовкае их к анализу
Путь к файлам:

 -   /datasets/visits_info_short.csv. Скачать датасет
 -   /datasets/orders_info_short.csv. Скачать датасет
 -   /datasets/costs_info_short.csv. Скачать датасет
 
- Шаг 2. Зададим функции для расчета и анализа LTV, ROI, удержания и конверсии

- Шаг 3. Проведение исследовательского анализа данных

    - Постройм профили пользователей. Определите минимальную и максимальную дату привлечения пользователей.
    Ответим на вопросы:
    - Из каких стран приходят посетители? Какие страны дают больше всего платящих пользователей?
    - Какими устройствами они пользуются? С каких устройств чаще всего заходят платящие пользователи?
    - По каким рекламным каналам шло привлечение пользователей? Какие каналы приносят больше всего платящих пользователей?.

- Шаг 4. Маркетинг
    Выясним:

    - Сколько денег потратили? Всего / на каждый источник / по времени
    - Сколько в среднем стоило привлечение одного покупателя из каждого источника?

- Шаг 5. Оценим окупаемость рекламы для привлечения пользователей

    С помощью LTV и ROI:
    - Проанализируем общую окупаемость рекламы;
    - Проанализируем окупаемость рекламы с разбивкой по устройствам;
    - Проанализируем окупаемость рекламы с разбивкой по странам;
    - Проанализируем окупаемость рекламы с разбивкой по рекламным каналам.

    Ответим на вопросы:
    - Окупается ли реклама, направленная на привлечение пользователей в целом? 
    - Какие устройства, страны и рекламные каналы могут оказывать негативное влияние на окупаемость рекламы?
    - Чем могут быть вызваны проблемы окупаемости? Изучите конверсию и удержание с разбивкой по устройствам, странам, рекламным каналам.

- Шаг 6. Напишим выводы


**Описание данных:**
Таблица visits_log_short (лог сервера с информацией о посещениях сайта):

    User Id — уникальный идентификатор пользователя
    Device — категория устройства пользователя
    Session start — дата и время начала сессии
    Session End — дата и время окончания сессии
    Channel — идентификатор рекламного источника, из которого пришел пользователь
    Region - страна пользователя

Таблица orders_log_short (информация о заказах):

    User Id — уникальный id пользователя, который сделал заказ
    Event Dt — дата и время покупки
    Revenue — выручка

Таблица costs_short (информация о затратах на маркетинг):

    Channel — идентификатор рекламного источника
    Dt — дата
    Costs — затраты на этот рекламный источник в этот день
