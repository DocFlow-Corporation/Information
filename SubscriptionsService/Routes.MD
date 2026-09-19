# Роуты Subscription Service

Базовый префикс сервиса - ***/subscriptions***

- ***GET /catalog*** - Получение каталога подписок

Пример:

```

{
  "Ultimate" => 
  [
    "price" => 40,
    "currency" => "USD",
    "description" => "Very cool subscription - buy it now!"
  ]
}

```

- ***POST /buy/{id подписки}*** - Покупка подписки

- ***GET /subscriptions/user/(active или all или -)/{user_id}*** - Получение подписок конкретного пользователя с возможностью выбора статуса

- ***GET /subscriptions/hassub/{user_id}*** - Проверка наличия активной подписки у пользователя


Возвращает ответ по типу:

```
{
  "isActive" => true
}

```
