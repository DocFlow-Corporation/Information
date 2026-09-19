# Роуты Subscription Service

Базовый префикс сервиса - ***/subscriptions***

- ***GET /catalog*** - Получение каталога подписок

Пример:

```

[
  { 
    "name" => "Ultimate",
    "price" => 40,
    "currency" => "USD",
    "description" => "Very cool subscription - buy it now!"
  }
]

```

- ***POST /buy/{id подписки}*** - Покупка подписки

- ***GET /user/(active или all или -)/{user_id}*** - Получение подписок конкретного пользователя с возможностью выбора статуса

```

[
  {
    "boughtAt" => "01.09.2026",
    "expiresAt" => "01.09.2027",
    "userId" => "1234",
    "plan" => "Premium"
  },
  {
    "boughtAt" => "01.09.2026",
    "expiresAt" => "01.09.2027",
    "userId" => "1234",
    "plan" => "Ultimate"
  },
{
    "boughtAt" => "20.12.2024",
    "expiresAt" => "20.12.2025",
    "userId" => "1234",
    "plan" => "Premium"
  }
]

```

- ***GET /hassub/{user_id}*** - Проверка наличия активной подписки у пользователя


Возвращает ответ по типу:

```
{
  "isActive" => true
}

```
