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
