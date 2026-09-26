### BUG-001 — Forgot Password возвращает 504 Gateway Time-out для валидного username

Priority: High

Related checklist item: AUTH-13

Environment:
- OrangeHRM OS 5.9
- Firefox 156
- macOS 27

Preconditions:
- Существует валидный username
- Пользователь находится на странице Forgot Password

Steps to Reproduce:

| # | Action |
|---|---|
| 1 | Открыть страницу Forgot Password |
| 2 | Ввести валидный username |
| 3 | Нажать Submit |
| 4 | Дождаться ответа сервера |

Expected Result:
- Запрос на сброс пароля обрабатывается успешно.
- Пользователь получает подтверждение, что запрос на сброс пароля отправлен.

Actual Result:
- Запрос не завершается успешно.
- После ожидания сервер возвращает `504 Gateway Time-out`.
- На странице ошибки отображается `nginx/1.18.0 (Ubuntu)`.

Technical Information:
- HTTP-статус: 504 Gateway Time-out
- Сервер: nginx/1.18.0 (Ubuntu)
