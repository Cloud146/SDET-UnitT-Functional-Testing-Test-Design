### Тест-кейс №04. Получение ошибки сервера

**Описание:** Проверка получения статуса существующего продукта при корректных параметрах запроса при возникновении ошибки на сервере.

**Предусловия**
- Введён валидный authToken
- Существует продукт с `{productId}`

**Тестовые данные:**
- Метод запроса: GET
- recalculate: true
- owner: Создатель
- region: Северо-Запад

**Шаги:**
1. Симулировать серверную ошибку
2. Отправить GET запрос к `/products/{productId}/status`

**Ожидаемый результат:**
- Приходит ответ с HTTP-кодом 500
- Тело ответа в формате JSON: `{"errorMessage": }`