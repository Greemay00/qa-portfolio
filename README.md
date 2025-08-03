# QA Portfolio

Примеры ручного тестирования популярных веб-приложений.

## 🧪 Содержание

- [OWASP Juice Shop](./juice-shop)
  - [Регистрация с Email в разном регистре](./bugs/email_case_sensitive_bug.md)
  - [Положительный сценарий: Успешная регистрация нового пользователя](./bugs/positive_registration.md)
  - [Негативный кейс: Проверка XSS-уязвимости на странице Customer Feedback](./bugs/xss_negative_case.md)
  - [Позитивный кейс: Авторизация через API (POST /rest/user/login)](./bugs/api_login_testcase_positive.md)
  - [Негативный кейс: Ошибка авторизации при вводе неверного пароля (POST /rest/user/login)](./bugs/api_login_testcase_negative.md)
  - [Баг-репорт: Ошибка 500 при добавлении несуществующего товара в корзину (POST /api/BasketItems)](./bugs/Basket_item_500_Bug_Report.md)
  - [Положительный сценарий: Проверка корректной работы функционала смены пароля в личном кабинете пользователя и валидации сохранённой сессии.](./bugs/psw_change_testcase.md)
  - [ Тест-кейс: Добавление и удаление товара из корзины.](./bugs/basket_item_add_remove.md)