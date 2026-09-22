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

## Sorting

### TC-ADM-014 — Сортировка пользователей по Username

Priority: Medium

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- В списке присутствуют несколько пользователей.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Нажать на Username | Пользователи отсортированы по Username по возрастанию |
| 2 | Повторно нажать на Username | Пользователи отсортированы по Username по убыванию |

---

### TC-ADM-015 — Сортировка пользователей по User Role

Priority: Medium

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- В списке присутствуют пользователи с разными ролями.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Нажать на User Role | Пользователи отсортированы по User Role по возрастанию |
| 2 | Повторно нажать на User Role | Пользователи отсортированы по User Role по убыванию |

---

### TC-ADM-016 — Сортировка пользователей по Employee Name

Priority: Medium

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- В списке присутствуют пользователи с разными именами сотрудников.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Нажать на Employee Name | Пользователи отсортированы по Employee Name по возрастанию |
| 2 | Повторно нажать на Employee Name | Пользователи отсортированы по Employee Name по убыванию |

---

### TC-ADM-017 — Сортировка пользователей по Status

Priority: Medium

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- В списке присутствуют пользователи с разными статусами.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Нажать на Status | Пользователи отсортированы по Status по возрастанию |
| 2 | Повторно нажать на Status | Пользователи отсортированы по Status по убыванию |

## Delete User

### TC-ADM-018 — Удаление пользователя

Priority: High

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- В списке присутствует пользователь, которого можно удалить.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Нажать кнопку удаления напротив пользователя | Отображается подтверждение удаления |
| 2 | Подтвердить удаление | Пользователь удалён из списка |

Postconditions:
- Удалённый пользователь отсутствует в списке.

---

## Edit User

### TC-ADM-019 — Переход к редактированию пользователя

Priority: High

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- В списке присутствует пользователь.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Нажать кнопку редактирования напротив пользователя | Выполняется переход на страницу редактирования выбранного пользователя |
| 2 | Проверить данные пользователя | Отображаются данные выбранного пользователя |

Postconditions:
- Открыта страница редактирования пользователя.

---

## Pagination

### TC-ADM-020 — Отображение пагинации

Priority: Medium

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Количество пользователей превышает количество записей, отображаемых на одной странице.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Проверить нижнюю часть списка пользователей | Отображается элемент пагинации |

Postconditions:
- Без изменений.

---

### TC-ADM-021 — Переход на следующую страницу

Priority: Medium

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Доступна следующая страница.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Нажать кнопку перехода на следующую страницу | Отображается следующая страница со списком пользователей |

Postconditions:
- Открыта следующая страница.

---

### TC-ADM-022 — Переход на предыдущую страницу

Priority: Medium

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта страница, следующая после первой.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Нажать кнопку перехода на предыдущую страницу | Отображается предыдущая страница со списком пользователей |

Postconditions:
- Открыта предыдущая страница.

---

### TC-ADM-023 — Отображение корректных пользователей на странице

Priority: Medium

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Доступно несколько страниц пользователей.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Перейти на следующую страницу | Отображаются пользователи, относящиеся к выбранной странице |
| 2 | Вернуться на предыдущую страницу | Отображаются пользователи предыдущей страницы |

Postconditions:
- Без изменений.

---

## Collapse System Users

### TC-ADM-024 — Сворачивание раздела System Users

Priority: Low

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Раздел System Users развёрнут.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Нажать стрелку сворачивания раздела System Users | Раздел System Users сворачивается |
| 2 | Проверить содержимое раздела | Содержимое раздела скрыто |

Postconditions:
- Раздел System Users свёрнут.
