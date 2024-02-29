# Фроленко Кирилл 253504
# Мобильное приложение для мониторинга финансов
# ОПИСАНИЕ ПРОЕКТА
## 1. Общие сведения
### 1.1 Назначение программы
Программа позволяет отслеживать текущее количество денежных средств и удобна для отображения информации о них.
## 2. Цели проекта
### 2.1 Основные цели проекта
Основная цель проекта состоит в разработке полноценного fullstack приложения, которое будет упрощать мониторинг личных финансов пользователей. Приложение позволит пользователям удобно вносить информацию об изменениях количества средств и предоставляет интуитивно понятный интерфейс для отображения финансовой информации. Дополнительно, приложение будет иметь функционал для автоматического обновления информации о финансах, что поможет упростить процесс отслеживания текущего состояния денежных средств. Также, приложение будет интегрировано с API для получения текущих курсов валют и будет предоставлять удобный калькулятор валют для преобразования суммы из одной валюты в другую. Все это позволит пользователям более эффективно контролировать свои финансы и принимать информированные решения по управлению бюджетом.
## 3. Описание проекта
### 3.1 Язык программирования
Для реализации проекта в основном будет использоваться язык kotlin
### 3.2 Функции и задачи
#### 3.2.1 Управление финансовыми операциями
Для управления финансовыми операциями будут использованы следующие методы:

get_finoperation_details() - получение списка всех финансовых операций пользователя.
get_finoperation_details(id) - получение конкретной финансовой операции по ее идентификатору.
create_finoperation(data) - создание новой финансовой операции на основе переданных данных.
update_finoperaction(id, data) - обновление данных о финансовой операции.
delete_finoperaction(id) - удаление финансовой операции.
parseSMSTransaction(smsText) - парсинг информации о транзакции из текста смс-уведомления.
#### 3.2.2 Статистика и отчеты
Для получения статистики и отчетов о финансовых операциях будут использованы следующие методы:

getSummary() - получение общей сводки по доходам и расходам пользователя.
getIncomeByCategory() - получение распределения доходов по категориям.
getExpenseByCategory() - получение распределения расходов по категориям.
getIncomeByMonth() - получение доходов по месяцам.
getExpenseByMonth() - получение расходов по месяцам.
#### 3.2.3 Курсы валют и калькулятор
Для получения актуальных курсов валют и использования калькулятора для преобразования суммы из одной валюты в другую будут использованы следующие методы:

getCurrencies() - получение списка доступных валют.
getExchangeRate(fromCurrency, toCurrency) - получение текущего курса обмена между указанными валютами.
convertCurrency(amount, fromCurrency, toCurrency) - преобразование суммы из одной валюты в другую на основе текущего курса обмена.
#### 3.2.4 Уведомления и предупреждения
Для отправки уведомлений и предупреждений пользователю будут использованы следующие методы:

getNotifications() - получение списка уведомлений пользователя.
createNotification(data) - создание нового уведомления на основе переданных данных.
updateNotification(id, data) - обновление данных о существующем уведомлении.
deleteNotification(id) - удаление уведомления.
#### 3.2.5 Локализация 
Для обеспечения поддержки различных языков пользователей и локализации приложения будут использованы следующие методы:

setLanguage(language) - установка языка приложения.
getTranslatedText(key) - получение перевода текста по ключу для текущего языка.
## 4. Модели данных
### 4.1 Финансовая операция
Идентификатор (ID)
Категория (Category) - категория, к которой относится операция
Тип операции (Type) - тип операции
Сумма (Amount) - сумма операции
Дата и время (DateTime) - дата и время операции
Идентификатор карты (CardID) - связь с конкретной картой, если операция связана с использованием карты
### 4.2 Уведомление
Идентификатор (ID)
Заголовок (Title) - заголовок уведомления
Текст (Text) - содержание уведомления
Дата и время создания (DateTime) - дата и время создания уведомления
### 4.3 Валюта
Идентификатор (ID)
Код (Code) - код валюты ("USD", "EUR" и т. д.)
Название (Name) - название валюты ("Доллар США", "Евро" и т. д.)
Текущий курс (ExchangeRate) - текущий курс обмена данной валюты по отношению к базовой валюте.
### 4.4 Операция
Идентификатор (ID)
Название (Name) - название категории операций
Описание (Description) - дополнительное описание категории
### 4.5 Бюджет
Идентификатор (ID)
Категория (Category) - категория, к которой относится бюджет
Максимальная сумма (Amount) - максимальная сумма, выделенная на данную категорию
Период (Period) - период, для которого устанавливается бюджет
Тип бюджета (BudgetType) - "наличные", "счета", "карты"
### 4.6 Карта
Идентификатор карты (CardID)
Тип карты (CardType) - например, "дебетовая", "кредитная", "предоплаченная" и т. д.
Номер карты (CardNumber) - зашифрованный или маскированный номер карты
Доступные средства (AvailableFunds) - текущая доступная сумма на карте
### 4.7 Настройки
Язык (language)
## 5 Диаграмма классов
<img width="589" alt="image" src="https://github.com/JankerPlay/OOP/assets/57415393/6a757dec-25aa-4b89-be0d-391d6e28f983">

