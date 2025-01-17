### Баг-репорт №01. Создание существующей папки

**Тип:** Баг

**Серьёзность:** Тривиальная

**Приоритет:** Низкий

**Предусловия:**
- Сформирован валидный OAuth токен
- На диске существует папка "test"

**Тестовые данные:**
- URL: https://cloud-api.yandex.net/v1/disk/resources?path=test
- Метод: PUT
- Headers: Content-Type - application/json
- Authorization: OAuth 2.0 - Request Headers - Header Prefix: OAuth

**Шаги:**
1. Отправить запрос с помощью POSTMAN 

**Ожидаемый результат:**
- Приходит ответ со статусом 400

**Фактический результат:**
- Приходит ответ со статусом 409 - Conflict и телом ответа

![Скриншот фактического результата(локальный)](\Task_T2\Screens\Screen4.png "Скриншот фактического результата")

![Скриншот фактического результата(гит)](https://github.com/Cloud146/SDET-UnitT-Functional-Testing-Test-Design/blob/TaskT2-BugReport/Task_T2/Screens/Screen4.png "Скриншот фактического результата")
