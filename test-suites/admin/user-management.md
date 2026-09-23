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

## Add User — Validation

### TC-ADM-025 — Username длиной более 5 символов

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username | Более 5 символов |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение длиной более 5 символов в Username | Значение отображается в поле |
| 2 | Перейти к следующему полю | Сообщение Should be at least 5 characters не отображается |

Postconditions:
- Очистить Username.


### TC-ADM-026 — Username длиной менее 5 символов

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username | Менее 5 символов |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение длиной менее 5 символов в Username | Значение отображается в поле |
| 2 | Перейти к следующему полю | Отображается сообщение Should be at least 5 characters |

Postconditions:
- Очистить Username.


### TC-ADM-027 — Username длиной 5 символов

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username | Ровно 5 символов |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение длиной 5 символов в Username | Значение отображается в поле |
| 2 | Перейти к следующему полю | Сообщение Should be at least 5 characters не отображается |

Postconditions:
- Очистить Username.


### TC-ADM-028 — Пустой Username

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username | Пустое значение |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Оставить Username пустым | Поле остаётся пустым |
| 2 | Нажать Save | Отображается сообщение об обязательном заполнении Username |

Postconditions:
- Очистить форму Add User.


### TC-ADM-029 — Username с пробелами

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username | Значение с пробелами |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение с пробелами в Username | Значение отображается в поле |
| 2 | Перейти к следующему полю | Отображается результат валидации Username |

Postconditions:
- Очистить Username.


### TC-ADM-030 — Username со специальными символами

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username | Значение со специальными символами |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение со специальными символами в Username | Значение отображается в поле |
| 2 | Перейти к следующему полю | Отображается результат валидации Username |

Postconditions:
- Очистить Username.


### TC-ADM-031 — Username на кириллице

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username | Значение на кириллице |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение на кириллице в Username | Значение отображается в поле |
| 2 | Перейти к следующему полю | Отображается результат валидации Username |

Postconditions:
- Очистить Username.


## Password — Validation

### TC-ADM-032 — Password длиной менее 7 символов

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | Менее 7 символов |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение длиной менее 7 символов в Password | Значение отображается в поле |
| 2 | Перейти к следующему полю | Отображается сообщение Should have at least 7 characters |

Postconditions:
- Очистить Password.


### TC-ADM-033 — Password длиной более 7 символов

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | Более 7 символов |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение длиной более 7 символов в Password | Значение отображается в поле |
| 2 | Перейти к следующему полю | Сообщение Should have at least 7 characters не отображается |

Postconditions:
- Очистить Password.


### TC-ADM-034 — Password длиной 7 символов

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | Ровно 7 символов |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение длиной 7 символов в Password | Значение отображается в поле |
| 2 | Перейти к следующему полю | Сообщение Should have at least 7 characters не отображается |

Postconditions:
- Очистить Password.


### TC-ADM-035 — Пустой Password

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | Пустое значение |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Оставить Password пустым | Поле остаётся пустым |
| 2 | Нажать Save | Отображается сообщение Required |

Postconditions:
- Очистить форму Add User.


### TC-ADM-036 — Password с пробелами

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | Значение с пробелами |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение с пробелами в Password | Значение отображается в поле |
| 2 | Перейти к следующему полю | Отображается результат валидации Password |

Postconditions:
- Очистить Password.


### TC-ADM-037 — Password со специальными символами

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | Значение со специальными символами |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение со специальными символами в Password | Значение отображается в поле |
| 2 | Перейти к следующему полю | Отображается результат валидации Password |

Postconditions:
- Очистить Password.


### TC-ADM-038 — Password на кириллице

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | Значение на кириллице |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение на кириллице в Password | Значение отображается в поле |
| 2 | Перейти к следующему полю | Отображается результат валидации Password |

Postconditions:
- Очистить Password.


### TC-ADM-039 — Password с одной строчной буквой

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | Значение с одной строчной буквой |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение с одной строчной буквой в Password | Значение отображается в поле |
| 2 | Перейти к следующему полю | Отображается результат валидации Password |

Postconditions:
- Очистить Password.


### TC-ADM-040 — Password без строчных букв

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | Значение без строчных букв |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение без строчных букв в Password | Значение отображается в поле |
| 2 | Перейти к следующему полю | Отображается результат валидации Password |

Postconditions:
- Очистить Password.


### TC-ADM-041 — Password с двумя строчными буквами

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | Значение с двумя строчными буквами |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение с двумя строчными буквами в Password | Значение отображается в поле |
| 2 | Перейти к следующему полю | Отображается результат валидации Password |

Postconditions:
- Очистить Password.

### TC-ADM-042 — Создание пользователя: Admin + invalid Employee Name + Enabled + valid Username + invalid Password + valid Confirm Password

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| User Role | Admin |
| Employee Name | Невалидный |
| Status | Enabled |
| Username | Валидный |
| Password | Невалидный |
| Confirm Password | Валидный |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Выбрать Admin в User Role | Выбрано значение Admin |
| 2 | Ввести несуществующий Employee Name | Employee Name отображается в поле |
| 3 | Выбрать Enabled в Status | Выбрано значение Enabled |
| 4 | Ввести валидный Username | Username отображается в поле |
| 5 | Ввести невалидный Password | Отображается результат валидации Password |
| 6 | Ввести валидный Confirm Password | Confirm Password отображается в поле |
| 7 | Нажать Save | Пользователь не создаётся, отображаются сообщения валидации соответствующих полей |

Postconditions:
- Очистить форму Add User.


### TC-ADM-043 — Создание пользователя: Admin + valid Employee Name + Disabled + invalid Username + valid Password + invalid Confirm Password

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| User Role | Admin |
| Employee Name | Валидный |
| Status | Disabled |
| Username | Невалидный |
| Password | Валидный |
| Confirm Password | Невалидный |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Выбрать Admin в User Role | Выбрано значение Admin |
| 2 | Ввести существующий Employee Name | Employee Name отображается в поле |
| 3 | Выбрать Disabled в Status | Выбрано значение Disabled |
| 4 | Ввести невалидный Username | Отображается результат валидации Username |
| 5 | Ввести валидный Password | Password отображается в поле |
| 6 | Ввести невалидный Confirm Password | Отображается результат валидации Confirm Password |
| 7 | Нажать Save | Пользователь не создаётся, отображаются сообщения валидации соответствующих полей |

Postconditions:
- Очистить форму Add User.


### TC-ADM-044 — Создание пользователя: ESS + invalid Employee Name + Enabled + invalid Username + valid Password + invalid Confirm Password

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| User Role | ESS |
| Employee Name | Невалидный |
| Status | Enabled |
| Username | Невалидный |
| Password | Валидный |
| Confirm Password | Невалидный |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Выбрать ESS в User Role | Выбрано значение ESS |
| 2 | Ввести несуществующий Employee Name | Employee Name отображается в поле |
| 3 | Выбрать Enabled в Status | Выбрано значение Enabled |
| 4 | Ввести невалидный Username | Отображается результат валидации Username |
| 5 | Ввести валидный Password | Password отображается в поле |
| 6 | Ввести невалидный Confirm Password | Отображается результат валидации Confirm Password |
| 7 | Нажать Save | Пользователь не создаётся, отображаются сообщения валидации соответствующих полей |

Postconditions:
- Очистить форму Add User.


### TC-ADM-045 — Создание пользователя: ESS + valid Employee Name + Enabled + invalid Username + invalid Password + valid Confirm Password

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| User Role | ESS |
| Employee Name | Валидный |
| Status | Enabled |
| Username | Невалидный |
| Password | Невалидный |
| Confirm Password | Валидный |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Выбрать ESS в User Role | Выбрано значение ESS |
| 2 | Ввести существующий Employee Name | Employee Name отображается в поле |
| 3 | Выбрать Enabled в Status | Выбрано значение Enabled |
| 4 | Ввести невалидный Username | Отображается результат валидации Username |
| 5 | Ввести невалидный Password | Отображается результат валидации Password |
| 6 | Ввести валидный Confirm Password | Confirm Password отображается в поле |
| 7 | Нажать Save | Пользователь не создаётся, отображаются сообщения валидации соответствующих полей |

Postconditions:
- Очистить форму Add User.


### TC-ADM-046 — Создание пользователя: ESS + valid Employee Name + Disabled + valid Username + invalid Password + invalid Confirm Password

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| User Role | ESS |
| Employee Name | Валидный |
| Status | Disabled |
| Username | Валидный |
| Password | Невалидный |
| Confirm Password | Невалидный |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Выбрать ESS в User Role | Выбрано значение ESS |
| 2 | Ввести существующий Employee Name | Employee Name отображается в поле |
| 3 | Выбрать Disabled в Status | Выбрано значение Disabled |
| 4 | Ввести валидный Username | Username отображается в поле |
| 5 | Ввести невалидный Password | Отображается результат валидации Password |
| 6 | Ввести невалидный Confirm Password | Отображается результат валидации Confirm Password |
| 7 | Нажать Save | Пользователь не создаётся, отображаются сообщения валидации соответствующих полей |

Postconditions:
- Очистить форму Add User.


### TC-ADM-047 — Создание пользователя: ESS + invalid Employee Name + Disabled + valid Username + valid Password + valid Confirm Password

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| User Role | ESS |
| Employee Name | Невалидный |
| Status | Disabled |
| Username | Валидный |
| Password | Валидный |
| Confirm Password | Валидный |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Add User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Выбрать ESS в User Role | Выбрано значение ESS |
| 2 | Ввести несуществующий Employee Name | Employee Name отображается в поле |
| 3 | Выбрать Disabled в Status | Выбрано значение Disabled |
| 4 | Ввести валидный Username | Username отображается в поле |
| 5 | Ввести валидный Password | Password отображается в поле |
| 6 | Ввести валидный Confirm Password | Confirm Password отображается в поле |
| 7 | Нажать Save | Пользователь не создаётся, отображается валидация Employee Name |

Postconditions:
- Очистить форму Add User.

## Edit User

### TC-ADM-048 — Username длиной более 5 символов

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username | Более 5 символов |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Edit User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение длиной более 5 символов в Username | Значение отображается в поле |
| 2 | Перейти к следующему полю | Сообщение Should be at least 5 characters не отображается |

Postconditions:
- Вернуть исходное значение Username.


### TC-ADM-049 — Username длиной 5 символов

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username | 5 символов |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Edit User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение длиной 5 символов в Username | Значение отображается в поле |
| 2 | Перейти к следующему полю | Сообщение Should be at least 5 characters не отображается |

Postconditions:
- Вернуть исходное значение Username.


### TC-ADM-050 — Username длиной менее 5 символов

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username | Менее 5 символов |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Edit User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение длиной менее 5 символов в Username | Значение отображается в поле |
| 2 | Перейти к следующему полю | Отображается сообщение Should be at least 5 characters |

Postconditions:
- Вернуть исходное значение Username.


### TC-ADM-051 — Пустой Username

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username | Пустое поле |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Edit User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Очистить Username | Поле Username становится пустым |
| 2 | Нажать Save | Отображается валидация обязательного поля Username |

Postconditions:
- Вернуть исходное значение Username.


### TC-ADM-052 — Username со специальными символами

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username | Значение со специальными символами |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Edit User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение со специальными символами в Username | Значение отображается в поле |
| 2 | Перейти к следующему полю | Отображается результат валидации Username |

Postconditions:
- Вернуть исходное значение Username.


### TC-ADM-053 — Username на кириллице

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username | Значение на кириллице |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Edit User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение на кириллице в Username | Значение отображается в поле |
| 2 | Перейти к следующему полю | Отображается результат валидации Username |

Postconditions:
- Вернуть исходное значение Username.


### TC-ADM-054 — Username на латинице

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username | Значение на латинице |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Edit User.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение на латинице в Username | Значение отображается в поле |
| 2 | Перейти к следующему полю | Отображается результат валидации Username |

Postconditions:
- Вернуть исходное значение Username.


## Edit User — Password Validation

### TC-ADM-055 — Password длиной более 7 символов

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | Более 7 символов |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Edit User.
- Включён Change Password ? → Yes.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение длиной более 7 символов в Password | Значение отображается в поле |
| 2 | Перейти к следующему полю | Сообщение Should have at least 7 characters не отображается |

Postconditions:
- Отключить Change Password ?.


### TC-ADM-056 — Password длиной 7 символов

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | 7 символов |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Edit User.
- Включён Change Password ? → Yes.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение длиной 7 символов в Password | Значение отображается в поле |
| 2 | Перейти к следующему полю | Сообщение Should have at least 7 characters не отображается |

Postconditions:
- Отключить Change Password ?.


### TC-ADM-057 — Password длиной менее 7 символов

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | Менее 7 символов |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Edit User.
- Включён Change Password ? → Yes.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение длиной менее 7 символов в Password | Значение отображается в поле |
| 2 | Перейти к следующему полю | Отображается сообщение Should have at least 7 characters |

Postconditions:
- Отключить Change Password ?.


### TC-ADM-058 — Пустой Password

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | Пустое поле |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Edit User.
- Включён Change Password ? → Yes.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Оставить Password пустым | Поле Password остаётся пустым |
| 2 | Нажать Save | Отображается валидация обязательного поля Password |

Postconditions:
- Отключить Change Password ?.


### TC-ADM-059 — Password с одной строчной буквой

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | Значение с одной строчной буквой |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Edit User.
- Включён Change Password ? → Yes.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение с одной строчной буквой в Password | Значение отображается в поле |
| 2 | Перейти к следующему полю | Отображается результат валидации Password |

Postconditions:
- Отключить Change Password ?.


### TC-ADM-060 — Password без строчных букв

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | Значение без строчных букв |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Edit User.
- Включён Change Password ? → Yes.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение без строчных букв в Password | Значение отображается в поле |
| 2 | Перейти к следующему полю | Отображается результат валидации Password |

Postconditions:
- Отключить Change Password ?.


### TC-ADM-061 — Password с двумя строчными буквами

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | Значение с двумя строчными буквами |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Edit User.
- Включён Change Password ? → Yes.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение с двумя строчными буквами в Password | Значение отображается в поле |
| 2 | Перейти к следующему полю | Отображается результат валидации Password |

Postconditions:
- Отключить Change Password ?.


### TC-ADM-062 — Password на кириллице

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | Значение на кириллице |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Edit User.
- Включён Change Password ? → Yes.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение на кириллице в Password | Значение отображается в поле |
| 2 | Перейти к следующему полю | Отображается результат валидации Password |

Postconditions:
- Отключить Change Password ?.


### TC-ADM-063 — Password на латинице

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | Значение на латинице |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Edit User.
- Включён Change Password ? → Yes.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести значение на латинице в Password | Значение отображается в поле |
| 2 | Перейти к следующему полю | Отображается результат валидации Password |

Postconditions:
- Отключить Change Password ?.


## Edit User — Confirm Password Validation

### TC-ADM-064 — Валидный Confirm Password

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | Валидное значение |
| Confirm Password | Совпадает с Password |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Открыта форма Edit User.
- Включён Change Password ? → Yes.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести валидный Password | Password отображается в поле |
| 2 | Ввести такое же значение в Confirm Password | Confirm Password отображается в поле |
| 3 | Перейти к следующему полю | Валидация Confirm Password проходит успешно |

Postconditions:
- Отключить Change Password ?.


### TC-ADM-065 — Невалидный Confirm Password

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | Валидное значение |
| Confirm Password | Не совпадает с Password |

Preconditions:
- Пользователь авторизован в системе.
- Открыта страница Admin → User Management.
- Включён Change Password ? → Yes.

Steps:

| # | Step | Expected Result |
|---|---|---|
| 1 | Ввести валидный Password | Password отображается в поле |
| 2 | Ввести отличающееся значение в Confirm Password | Confirm Password отображается в поле |
| 3 | Перейти к следующему полю | Отображается результат валидации Confirm Password |

Postconditions:
- Отключить Change Password ?.
