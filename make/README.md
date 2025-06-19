# Подключение шаблона в Make: 5 шагов

## 1. Импорт шаблона и базовые настройки
1.1. **Создайте новый аккаунт в Make** (если у вас его нет): [Регистрация в Make](https://www.make.com/en/register?pc=aibot)

1.2. Перейдите в **раздел "Сценарии"** и **импортируйте шаблон [make-wazzup/blueprint-openai-assistant-wazzup.json](https://github.com/shorin-nikita/PrideAIBot/blob/main/make-wazzup/blueprint-openai-assistant-wazzup.json)**.

1.3. Откройте новый сценарий, нажмите на **три точки внизу** → **Импортировать Blueprint**.

## 2. Создание базы данных
2.1. Откройте второй модуль в сценарии и нажмите **Create A Data Store**.

2.2. Назовите базу **thread_id** (используйте маленькие буквы и нижнее подчёркивание, то есть формат snake_case).

2.3. Добавьте **первый элемент** структуры **thread_id**.

2.4. Сохраните изменения.

2.5. Подключите эту базу в два других модуля сценария.

## 3. Подключение **OpenAI**
3.1. Авторизуйтесь на сайте OpenAI.com.

3.2. Создайте нового ИИ Ассистента [в специальной вкладке](https://platform.openai.com/assistants).

3.3. Добавьте [Системный Промпт](https://github.com/shorin-nikita/PrideAIBot/blob/main/make-wazzup/system-prompt-oak.txt), активируйте векторную базу данных **Tool -> File Search** и добавьте [файл с базой знаний](https://github.com/shorin-nikita/PrideAIBot/blob/main/make-wazzup/knowledge-base-oak.json).

3.4. Сгенерируйте новый API ключ в разделе [API key](https://platform.openai.com/api-keys) и добавьте его в сценарий в Make.

## 4. Интеграция с **WhatsApp/Telegram**
4.1. **Зарегистрируйтесь в Wazzup** (если еще не сделали этого): [Регистрация в Wazzup](https://wazzup24.com/?utm_p=qzzBpM)

4.2. Подключите **Telegram-бота** через [**@BotFather**](https://t.me/BotFather) и скопируйте **API-ключ**.

4.3. Вставьте **API-ключ** в **Wazzup**.

4.4. Перейдите в **вкладку "Интеграция с CRM"** и выберите **API** в **Wazzup**, получите **API-ключ** и добавьте его в **Make**.

4.5. Вставьте **API-ключ** в параметр **WAZZAP_API_KEY** в Make, который находится в нижней панели во вкладке **"Scenario inputs"**.

## 5. Привязка **Webhook**
5.1. Нажмите на **первый красный кружок** в **Make** и создайте **Webhook**.

5.2. Сохраните адрес **Webhook**.

5.3. Дублируйте вкладку **Make** и импортируйте **второй шаблон [make-wazzup/blueprint-connect-wazzup.json](https://github.com/shorin-nikita/PrideAIBot/blob/main/make-wazzup/blueprint-connect-wazzup.json)**.

5.4. Вставьте **API-ключ от Wazzup** в параметр **WAZZAP_API_KEY** в Make, который находится в нижней панели во вкладке **"Scenario inputs"**.

5.5. Вставьте **Webhook-адрес**, который создали на шаге 5.1, и добавьте его в переменную **webhook_url**.

5.6. Запустите сценарий **Run Once**.

5.7. Получите **код 200** (означает успешную привязку).

## Тестирование и проверка
• Запустите **Telegram-бота**.

• Отправьте сообщение.

• Проверьте движение запроса в **Make**.

• Убедитесь, что **ИИ-ассистент** сохраняет нить диалога (**Thread ID**).


## **Пошаговая видео-инструкция здесь:**

[![YouTube Видео-инструкция](https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white)](https://www.youtube.com/watch?v=nhY62MFI8Mc&t)

## Поздравляю, ваш **ИИ-ассистент** интегрирован в **Телеграм**!

Если вы хотите работать с проверенными шаблонами и промптами, а также развиваться в AI-автоматизации – добро пожаловать в [**PrideAIBot**](https://t.me/PrideAIBot)!
