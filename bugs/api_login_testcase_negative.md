## ❌ Негативный кейс: Ошибка авторизации при вводе неверного пароля (POST /rest/user/login)

### 📌 Описание
Проверка, что пользователь **не может авторизоваться** через API OWASP Juice Shop при вводе **неверного пароля**.

---

### 🧪 Шаги:
1. Открыть Postman.
2. Создать новый POST-запрос по адресу:
   ```
   http://localhost:3000/rest/user/login
   ```
3. Вкладка **Headers**:
   | Key           | Value             |
   |---------------|-------------------|
   | Content-Type  | application/json  |

4. Вкладка **Body** → **raw** → **JSON**:
   ```json
   {
     "email": "testuser@mail.ru",
     "password": "123$Y$admin"
   }
   ```
5. Нажать **Send** и проверить ответ.

---

### ❗ Ожидаемый результат
- Статус ответа: `401 Unauthorized`
- В теле ответа отображается сообщение об ошибке: `Invalid email or password.`
- Токен авторизации (JWT) **не выдается**.

### 📷 Скриншот
https://imgur.com/a/8ewOUZn
---

### 📦 Среда
- API: OWASP Juice Shop
- Версия: последняя (Docker)
- Инструмент: Postman 10+
- ОС: Windows 11 / Ubuntu 22.04

---

### 💬 Комментарии
- Такой тест позволяет проверить корректность обработки некорректных логинов и безопасность авторизации.
- Вариант для расширения: проверить сценарий с отсутствием пароля, пустым телом запроса, или отсутствием заголовка `Content-Type`.
