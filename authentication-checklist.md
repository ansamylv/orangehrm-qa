## Test Information

| Parameter   | Value                |
| ----------- | -------------------- |
| Environment | OrangeHRM Demo OS 5.9 |
| Date        | 20.09.2026           |
| Browser     | Firefox 156          |
| OS          | macOS 27             |

## Login

### Обязательность полей

| ID       | Check                      | Status  |
| -------- | -------------------------- | ------- |
| AUTH-001 | Пустой Username            | Not Run |
| AUTH-002 | Пустой Password            | Not Run |
| AUTH-003 | Пустые Username и Password | Not Run |

### Проверка учётных данных

| ID       | Check                                     | Status  |
| -------- | ----------------------------------------- | ------- |
| AUTH-004 | Валидный Username + невалидный Password   | Not Run |
| AUTH-005 | Невалидный Username + валидный Password   | Not Run |
| AUTH-006 | Валидный Username + валидный Password     | Not Run |
| AUTH-007 | Невалидный Username + невалидный Password | Not Run |

## Social Media

| ID       | Check              | Status  |
| -------- | ------------------ | ------- |
| AUTH-008 | Переход в LinkedIn | Not Run |
| AUTH-009 | Переход в Facebook | Not Run |
| AUTH-010 | Переход в Twitter  | Not Run |
| AUTH-011 | Переход в YouTube  | Not Run |

## Forgot Password

### Username

| ID       | Check               | Status  |
| -------- | ------------------- | ------- |
| AUTH-012 | Пустой Username     | Not Run |
| AUTH-013 | Валидный Username   | Not Run |
| AUTH-014 | Невалидный Username | Not Run |

### Навигация

| ID       | Check                                             | Status  |
| -------- | ------------------------------------------------- | ------- |
| AUTH-015 | Кнопка Cancel возвращает на страницу авторизации | Not Run |

## Google Authentication

| ID | Check | Status |
|---|---|---|
| AUTH-016 | Отображение кнопки Sign in with Google | Not Run |
| AUTH-017 | Переход к авторизации через Google | Not Run |
