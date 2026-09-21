# Admin — User Management

## Test Information

| Parameter | Value |
|---|---|
| Environment | OrangeHRM Demo OS 5.9 |
| Browser | Firefox 156 |
| OS | macOS 27 |
| Module | Admin → User Management |

---

## Filtering

### TC-ADM-001 — Фильтрация: существующий Username + Admin + несуществующий Employee Name + Enabled

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username | Существующий |
| User Role | Admin |
| Employee Name | Несуществующий |
| Status | Enabled |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести существующий Username | Username отображается в поле |
| 2 | Выбрать Admin в User Role | Выбрано значение Admin |
| 3 | Ввести несуществующий Employee Name | Employee Name отображается в поле |
| 4 | Выбрать Enabled в Status | Выбрано значение Enabled |
| 5 | Нажать Search | Отображаются пользователи, соответствующие заданным условиям. При отсутствии совпадений отображается пустой результат |

Postconditions:
- Нажать Reset для сброса фильтров.

---

### TC-ADM-002 — Фильтрация: существующий Username + ESS + существующий Employee Name + Disabled

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username | Существующий |
| User Role | ESS |
| Employee Name | Существующий |
| Status | Disabled |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести существующий Username | Username отображается в поле |
| 2 | Выбрать ESS в User Role | Выбрано значение ESS |
| 3 | Ввести существующий Employee Name | Employee Name отображается в поле |
| 4 | Выбрать Disabled в Status | Выбрано значение Disabled |
| 5 | Нажать Search | Отображаются только пользователи, соответствующие заданным условиям |

Postconditions:
- Нажать Reset для сброса фильтров.

---

### TC-ADM-003 — Фильтрация: несуществующий Username + Admin + несуществующий Employee Name + Disabled

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username | Несуществующий |
| User Role | Admin |
| Employee Name | Несуществующий |
| Status | Disabled |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести несуществующий Username | Username отображается в поле |
| 2 | Выбрать Admin в User Role | Выбрано значение Admin |
| 3 | Ввести несуществующий Employee Name | Employee Name отображается в поле |
| 4 | Выбрать Disabled в Status | Выбрано значение Disabled |
| 5 | Нажать Search | Отображается пустой результат, если пользователей, соответствующих всем условиям, нет |

Postconditions:
- Нажать Reset для сброса фильтров.

---

### TC-ADM-004 — Фильтрация: несуществующий Username + ESS + существующий Employee Name + Enabled

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username | Несуществующий |
| User Role | ESS |
| Employee Name | Существующий |
| Status | Enabled |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести несуществующий Username | Username отображается в поле |
| 2 | Выбрать ESS в User Role | Выбрано значение ESS |
| 3 | Ввести существующий Employee Name | Employee Name отображается в поле |
| 4 | Выбрать Enabled в Status | Выбрано значение Enabled |
| 5 | Нажать Search | Отображается пустой результат, если пользователей, соответствующих всем условиям, нет |

Postconditions:
- Нажать Reset для сброса фильтров.

---

### TC-ADM-005 — Фильтрация: несуществующий Username + Admin + существующий Employee Name + Disabled

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username | Несуществующий |
| User Role | Admin |
| Employee Name | Существующий |
| Status | Disabled |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести несуществующий Username | Username отображается в поле |
| 2 | Выбрать Admin в User Role | Выбрано значение Admin |
| 3 | Ввести существующий Employee Name | Employee Name отображается в поле |
| 4 | Выбрать Disabled в Status | Выбрано значение Disabled |
| 5 | Нажать Search | Отображается пустой результат, если пользователей, соответствующих всем условиям, нет |

Postconditions:
- Нажать Reset для сброса фильтров.

---

### TC-ADM-006 — Фильтрация: существующий Username + ESS + несуществующий Employee Name + Disabled

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username | Существующий |
| User Role | ESS |
| Employee Name | Несуществующий |
| Status | Disabled |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести существующий Username | Username отображается в поле |
| 2 | Выбрать ESS в User Role | Выбрано значение ESS |
| 3 | Ввести несуществующий Employee Name | Employee Name отображается в поле |
| 4 | Выбрать Disabled в Status | Выбрано значение Disabled |
| 5 | Нажать Search | Отображается пустой результат, если пользователей, соответствующих всем условиям, нет |

Postconditions:
- Нажать Reset для сброса фильтров.


## Test Information

| Parameter | Value |
|---|---|
| Environment | OrangeHRM Demo OS 5.9 |
| Browser | Firefox 156 |
| OS | macOS 27 |
| Module | Admin → User Management |

---

## Reset

### TC-ADM-007 — Сброс параметров фильтрации

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username | Существующий |
| User Role | Admin |
| Employee Name | Существующий |
| Status | Enabled |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Заполнить Username | Значение отображается в поле |
| 2 | Выбрать Admin в User Role | Выбрано значение Admin |
| 3 | Заполнить Employee Name | Значение отображается в поле |
| 4 | Выбрать Enabled в Status | Выбрано значение Enabled |
| 5 | Нажать Reset | Все поля фильтрации очищены |

Postconditions:
- Фильтры сброшены.

---

## Search

### TC-ADM-008 — Поиск пользователей по указанным параметрам

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Username | Существующий |
| User Role | Admin |
| Employee Name | Существующий |
| Status | Enabled |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Заполнить Username | Значение отображается в поле |
| 2 | Выбрать Admin в User Role | Выбрано значение Admin |
| 3 | Заполнить Employee Name | Значение отображается в поле |
| 4 | Выбрать Enabled в Status | Выбрано значение Enabled |
| 5 | Нажать Search | Отображаются пользователи, соответствующие указанным параметрам |

Postconditions:
- Нажать Reset для сброса фильтров.

---

## Add User

### TC-ADM-009 — Отображение кнопки Add User

Priority: Medium

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Проверить область управления списком пользователей | Кнопка Add User отображается |

Postconditions:
- Без изменений.

---

### TC-ADM-010 — Переход к созданию пользователя

Priority: High

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Нажать Add User | Выполняется переход на страницу создания пользователя |

Postconditions:
- Открыта страница создания пользователя.

---

## Checkboxes

### TC-ADM-011 — Отображение кнопки удаления при выборе пользователей

Priority: Medium

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- В списке присутствует хотя бы один пользователь.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Выбрать чекбокс одного пользователя | Пользователь выбран |
| 2 | Проверить область управления списком | Отображается кнопка удаления выбранных пользователей |

Postconditions:
- Выбранный пользователь не удалён.

---

### TC-ADM-012 — Выбор нескольких пользователей

Priority: Medium

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- В списке присутствует несколько пользователей.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Выбрать чекбокс первого пользователя | Пользователь выбран |
| 2 | Выбрать чекбокс второго пользователя | Второй пользователь выбран |
| 3 | Проверить область управления списком | Отображается кнопка удаления выбранных пользователей |

Postconditions:
- Выбранные пользователи не удалены.

---

## Delete Selected

### TC-ADM-013 — Удаление выбранных пользователей

Priority: High

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- В списке присутствуют пользователи, которых можно удалить.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Выбрать чекбоксы нескольких пользователей | Пользователи выбраны |
| 2 | Нажать кнопку удаления выбранных пользователей | Отображается подтверждение удаления |
| 3 | Подтвердить удаление | Выбранные пользователи удалены из списка |

Postconditions:
- Выбранные пользователи отсутствуют в списке.
