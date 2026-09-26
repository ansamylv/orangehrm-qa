## Test Information

| Parameter   | Value                 |
| ----------- | --------------------- |
| Environment | OrangeHRM Demo OS 5.9 |
| Date        | 20.09.2026             |
| Browser     | Firefox 156           |
| OS          | macOS 27              |

## Login

### Обязательность полей

| ID       | Check                       | Status | Comment |
| -------- | ---------------------------- | ------ | ------- |
| AUTH-001 | Пустой Username               | Passed |         |
| AUTH-002 | Пустой Password                | Passed |         |
| AUTH-003 | Пустые Username и Password     | Passed |         |

### Проверка учётных данных

| ID       | Check                                      | Status | Comment |
| -------- | -------------------------------------------- | ------ | ------- |
| AUTH-004 | Валидный Username + невалидный Password       | Passed |         |
| AUTH-005 | Невалидный Username + валидный Password       | Passed |         |
| AUTH-006 | Валидный Username + валидный Password         | Passed |         |
| AUTH-007 | Невалидный Username + невалидный Password     | Passed |         |

## Social Media

| ID       | Check               | Status | Comment |
| -------- | -------------------- | ------ | ------- |
| AUTH-008 | Переход в LinkedIn    | Passed |         |
| AUTH-009 | Переход в Facebook    | Passed |         |
| AUTH-010 | Переход в Twitter     | Passed |         |
| AUTH-011 | Переход в YouTube     | Passed |         |

## Forgot Password

### Username

| ID       | Check                | Status | Comment |
| -------- | ---------------------- | ------ | ------- |
| AUTH-012 | Пустой Username         | Passed |         |
| AUTH-013 | Валидный Username       | Failed | Форма зависает и возвращает `504 Gateway Time-out` вместо подтверждения отправки письма. См. BUG-001. |
| AUTH-014 | Невалидный Username     | Passed |

### Навигация

| ID       | Check                                              | Status | Comment |
| -------- | ---------------------------------------------------- | ------ | ------- |
| AUTH-015 | Кнопка Cancel возвращает на страницу авторизации      | Passed |         |
