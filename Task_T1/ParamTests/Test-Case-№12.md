### Тест-кейс №12. Проверка параметров по комбинации false - Создатель - Сибирь

**Описание:** Проверка получения статуса существующего продукта при корректных параметрах запроса.
Комбинация 6: false - Создатель - Сибирь

**Предусловия**
- Введён валидный authToken
- Существует продукт с `{productId}`

**Тестовые данные:**
- Метод запроса: GET
- recalculate: false
- owner: Создатель
- region: Сибирь

**Шаги:**
1. Отправить GET запрос к `/products/{productId}/status`

**Ожидаемый результат:**
- Приходит ответ с HTTP-кодом 200
- Тело ответа в формате JSON: `{ "productStatus": 1 }` или `{ "productStatus": 0 }`