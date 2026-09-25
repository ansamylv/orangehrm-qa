### TC-LEAVE-LIST-001 — Подготовка тестовых данных для фильтрации

Priority: High

Test Data:

| # | Сотрудник (Sub Unit) | Leave Type | Статус |
|---|---|---|---|
| 1 | Employee A (Finance) | CAN - Vacation | Pending Approval |
| 2 | Employee B (Engineering) | CAN - Personal | Scheduled |
| 3 | Employee C (Sales & Marketing) | US - Bereavement | Taken |
| 4 | Employee D (Human Resources) | US - Personal | Rejected |
| 5 | Employee E (Client Services) | CAN - Bereavement | Cancelled |

Preconditions:
- Пользователь авторизован с правами на Leave → Assign Leave.
- Определены сотрудники, принадлежащие разным Sub Unit (уточнить в PIM → Employee List при необходимости).

Steps:

| # | Action |
|---|---|
| 1 | Перейти в Leave → Assign Leave |
| 2 | Создать заявку по строке 1 таблицы Test Data (сотрудник, тип, даты в пределах 2026 года) |
| 3 | Повторить для строк 2–5 |
| 4 | Если статус нельзя задать напрямую при создании, изменить его через действия в Leave List (Approve / Reject / Cancel) до нужного значения из таблицы |
| 5 | Перейти в Leave List, убрать все фильтры кроме обязательного Status (выбрать все статусы), нажать Search |

Expected Result:
- Все 5 заявок отображаются в списке с соответствующими статусами, типами и сотрудниками.

Postconditions:
- В системе существуют 5 заявок на отпуск с разными статусами, типами (CAN/US) и Sub Unit — используются как база для последующих тестов.

### TC-LEAVE-LIST-002 — Иконка календаря открывает выбор даты

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Проверяемое поле | From Date, To Date (по очереди) |

Preconditions:
- Пользователь авторизован.
- Открыта Leave → Leave List.

Steps:

| # | Action |
|---|---|
| 1 | Нажать на иконку календаря рядом с From Date |
| 2 | Убедиться, что открылся виджет выбора даты, закрыть его |
| 3 | Нажать на иконку календаря рядом с To Date |
| 4 | Убедиться, что открылся виджет выбора даты |

Expected Result:
- В обоих случаях открывается виджет календаря.
- Виджет закрывается при выборе даты или клике вне его области.

Postconditions:
- Данные в системе не изменились.

### TC-LEAVE-LIST-003 — Навигация стрелками в виджете календаря

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Проверяемое поле | From Date |

Preconditions:
- Пользователь авторизован.
- Открыта Leave → Leave List.
- Открыт виджет календаря для From Date.

Steps:

| # | Action |
|---|---|
| 1 | Нажать стрелку «следующий месяц» несколько раз подряд, включая переход через границу года (декабрь → январь) |
| 2 | Нажать стрелку «предыдущий месяц» несколько раз подряд, включая переход через границу года (январь → декабрь) |

Expected Result:
- При каждом нажатии отображаемый месяц и год корректно меняются.
- Сетка дней обновляется в соответствии с выбранным месяцем.
- Переход через границу года меняет год в заголовке виджета.

Postconditions:
- Данные в системе не изменились.

### TC-LEAVE-LIST-004 — Выбор корректной даты через виджет календаря

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| From Date | любая дата текущего или прошлого месяца |
| To Date | дата позже From Date |

Preconditions:
- Пользователь авторизован.
- Открыта Leave → Leave List.
- В Status выбран хотя бы один параметр (например, Pending Approval).

Steps:

| # | Action |
|---|---|
| 1 | Открыть виджет для From Date, выбрать дату |
| 2 | Открыть виджет для To Date, выбрать дату позже From Date |
| 3 | Нажать Search |

Expected Result:
- Выбранные даты отображаются в полях в формате YYYY-MM-DD.
- Поиск выполняется без ошибок.

Postconditions:
- Данные в системе не изменились.

### TC-LEAVE-LIST-005 — Ввод некорректного формата даты вручную

Priority: High

Test Data:

| # | Значение | Проблема |
|---|---|---|
| 1 | 2026-31-12 | день и месяц перепутаны местами (воспроизведённый дефект) |
| 2 | 2026-13-01 | несуществующий месяц (13) |
| 3 | 2026-02-30 | несуществующий день для февраля |

Preconditions:
- Пользователь авторизован.
- Открыта Leave → Leave List.
- В Status выбран хотя бы один параметр.

Steps:

| # | Action |
|---|---|
| 1 | Вручную ввести значение 1 в текстовое поле From Date (без использования виджета), нажать Search |
| 2 | Зафиксировать результат, вернуть поле в валидное состояние |
| 3 | Повторить шаги 1–2 для значений 2 и 3 |
| 4 | Повторить весь набор (значения 1–3) для поля To Date |

Expected Result:
- Под соответствующим полем отображается сообщение об ошибке формата даты.
- Поиск не выполняется, а если выполняется — не возвращает результат по несуществующей дате.
- Система не выдаёт технических ошибок (500, белый экран).

Postconditions:
- Данные в системе не изменились.

### TC-LEAVE-LIST-006 — To Date раньше, чем From Date

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| From Date | 2026-06-01 |
| To Date | 2026-01-01 |

Preconditions:
- Пользователь авторизован.
- Открыта Leave → Leave List.
- В Status выбран хотя бы один параметр.

Steps:

| # | Action |
|---|---|
| 1 | Вручную ввести From Date и To Date из Test Data |
| 2 | Нажать Search |
| 3 | Зафиксировать результат |
| 4 | Открыть виджет календаря для To Date при уже выбранном From Date = 2026-06-01 и проверить, доступны ли для выбора даты раньше 2026-06-01 |

Expected Result:
- При ручном вводе отображается сообщение об ошибке (To Date не может быть раньше From Date), поиск не выполняется.
- В виджете календаря даты раньше From Date либо недоступны для выбора, либо доступны — зафиксировать соответствие этому же правилу.

Postconditions:
- Данные в системе не изменились.

### TC-LEAVE-LIST-007 — Добавление и удаление тегов в Show Leave with Status

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Теги для добавления | Scheduled, Taken |

Preconditions:
- Пользователь авторизован.
- Открыта Leave → Leave List.
- В поле Status присутствует тег по умолчанию (Pending Approval).

Steps:

| # | Action |
|---|---|
| 1 | Открыть дропдаун Status, выбрать Scheduled |
| 2 | Открыть дропдаун снова, выбрать Taken |
| 3 | Нажать ✕ на теге Scheduled |
| 4 | Открыть дропдаун и попытаться выбрать Taken повторно |

Expected Result:
- После шагов 1–2 отображаются три тега: Pending Approval, Scheduled, Taken.
- После шага 3 тег Scheduled удалён, остальные два сохранились.
- На шаге 4 уже выбранный Taken либо скрыт из списка дропдауна, либо неактивен; дубликат тега не создаётся.

Postconditions:
- Данные в системе не изменились.

### TC-LEAVE-LIST-008 — Status без единого выбранного параметра

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Show Leave with Status | все теги удалены |
| Остальные поля | значения по умолчанию |

Preconditions:
- Пользователь авторизован.
- Открыта Leave → Leave List.

Steps:

| # | Action |
|---|---|
| 1 | Удалить все теги в поле Status через ✕ |
| 2 | Нажать Search |

Expected Result:
- Под полем Status отображается сообщение об обязательности поля (Required).
- Поиск не выполняется.

Postconditions:
- Данные в системе не изменились.

### TC-LEAVE-LIST-009 — Дропдаун Leave Type отображает группы CAN/US и позволяет выбрать значение

Priority: Low

Test Data:

| Parameter | Value |
|---|---|
| Значение 1 | любой пункт из группы CAN |
| Значение 2 | любой пункт из группы US |

Preconditions:
- Пользователь авторизован.
- Открыта Leave → Leave List.

Steps:

| # | Action |
|---|---|
| 1 | Открыть дропдаун Leave Type, убедиться в наличии групп CAN и US |
| 2 | Выбрать значение 1 |
| 3 | Открыть дропдаун снова, выбрать значение 2 |

Expected Result:
- Группы CAN и US отображаются с соответствующими пунктами.
- Выбор пункта из любой группы обновляет значение поля.

Postconditions:
- Данные в системе не изменились.

### TC-LEAVE-LIST-010 — Валидное значение Employee Name через автокомплит

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Employee Name | часть имени существующего сотрудника |

Preconditions:
- Пользователь авторизован.
- Открыта Leave → Leave List.

Steps:

| # | Action |
|---|---|
| 1 | Ввести часть имени существующего сотрудника в поле Employee Name |
| 2 | Выбрать сотрудника из списка подсказок |
| 3 | Нажать Search |

Expected Result:
- При вводе появляются подсказки, соответствующие введённой части имени.
- После выбора поле заполняется полным именем.
- Кнопка Search доступна, поиск выполняется без ошибок.

Postconditions:
- Данные в системе не изменились.

### TC-LEAVE-LIST-011 — Невалидное значение Employee Name блокирует Search

Priority: High

Test Data:

| # | Значение |
|---|---|
| 1 | несуществующее имя (полностью придуманное) |
| 2 | набор спецсимволов (!@#$%) |
| 3 | текст введён, но подсказка из списка не выбрана |

Preconditions:
- Пользователь авторизован.
- Открыта Leave → Leave List.

Steps:

| # | Action |
|---|---|
| 1 | Ввести значение 1 в Employee Name, не выбирая ничего из подсказок, нажать Search |
| 2 | Зафиксировать результат, очистить поле |
| 3 | Повторить шаги 1–2 для значений 2 и 3 |

Expected Result:
- Для всех трёх вариантов кнопка Search заблокирована либо её нажатие не выполняет поиск, под полем отображается сообщение об ошибке.
- Поведение одинаково для всех трёх вариантов.

Postconditions:
- Данные в системе не изменились.

### TC-LEAVE-LIST-012 — Сотрудник относится к выбранному Sub Unit

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Sub Unit | Finance |
| Employee Name | сотрудник, реально состоящий в Finance |

Preconditions:
- Пользователь авторизован.
- Открыта Leave → Leave List.
- Известен сотрудник, состоящий в Sub Unit Finance.

Steps:

| # | Action |
|---|---|
| 1 | Выбрать Sub Unit = Finance |
| 2 | Ввести и выбрать сотрудника из Finance в Employee Name |
| 3 | Нажать Search |

Expected Result:
- Сотрудник принимается полем без ошибок.
- Поиск выполняется, в результатах (если есть заявки) отображаются только записи этого сотрудника.

Postconditions:
- Данные в системе не изменились.

### TC-LEAVE-LIST-013 — Сотрудник не относится к выбранному Sub Unit

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Sub Unit | Finance |
| Employee Name | сотрудник из Engineering |

Preconditions:
- Пользователь авторизован.
- Открыта Leave → Leave List.
- Известен сотрудник, состоящий в Sub Unit Engineering.

Steps:

| # | Action |
|---|---|
| 1 | Выбрать Sub Unit = Finance |
| 2 | Попытаться ввести и выбрать сотрудника из Engineering в Employee Name |
| 3 | Если выбор удался, нажать Search |

Expected Result:
- Автокомплит либо не предлагает сотрудника из другого Sub Unit после выбора Finance, либо предлагает, но Search в этом случае возвращает «No Records Found» без ошибок.

Postconditions:
- Данные в системе не изменились.

### TC-LEAVE-LIST-014 — Include Past Employees выключен: уволенный сотрудник не находится

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Include Past Employees | OFF |
| Employee Name | имя уволенного сотрудника |

Preconditions:
- Пользователь авторизован.
- Открыта Leave → Leave List.
- В системе есть уволенный сотрудник с историей заявок на отпуск.

Steps:

| # | Action |
|---|---|
| 1 | Убедиться, что переключатель Include Past Employees выключен |
| 2 | Ввести имя уволенного сотрудника в Employee Name |

Expected Result:
- Автокомплит не предлагает уволенного сотрудника, либо поле не позволяет выбрать его для поиска.

Postconditions:
- Данные в системе не изменились.

### TC-LEAVE-LIST-015 — Include Past Employees включён: уволенный сотрудник находится

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Include Past Employees | ON |
| Employee Name | имя уволенного сотрудника |

Preconditions:
- Пользователь авторизован.
- Открыта Leave → Leave List.
- В системе есть уволенный сотрудник с историей заявок на отпуск.

Steps:

| # | Action |
|---|---|
| 1 | Включить переключатель Include Past Employees |
| 2 | Ввести имя уволенного сотрудника в Employee Name и выбрать его из подсказок |
| 3 | Нажать Search |

Expected Result:
- Автокомплит предлагает уволенного сотрудника.
- Search возвращает его заявки на отпуск, если они существуют.

Postconditions:
- Данные в системе не изменились.

### TC-LEAVE-LIST-016 — Кнопка Reset возвращает форму к значениям по умолчанию

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Все поля | изменены на нестандартные значения перед Reset |

Preconditions:
- Пользователь авторизован.
- Открыта Leave → Leave List.

Steps:

| # | Action |
|---|---|
| 1 | Изменить From Date, To Date, добавить/убрать теги в Status, выбрать Leave Type, ввести Employee Name, выбрать Sub Unit, включить Include Past Employees |
| 2 | Нажать Reset |

Expected Result:
- Все поля возвращаются к значениям по умолчанию (Status содержит только тег по умолчанию, Leave Type и Sub Unit — «-- Select --», Employee Name пусто, Include Past Employees — OFF, даты — к значениям по умолчанию).
- Таблица результатов также сбрасывается.

Postconditions:
- Данные в системе не изменились.

### TC-LEAVE-LIST-017 — Search возвращает записи по заданным фильтрам (happy path)

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Status | Pending Approval |
| From Date / To Date | диапазон, покрывающий тестовые данные из TC-LEAVE-LIST-001 |
| Остальные поля | значения по умолчанию |

Preconditions:
- Пользователь авторизован.
- Открыта Leave → Leave List.
- Выполнен TC-LEAVE-LIST-001 (тестовые данные существуют).

Steps:

| # | Action |
|---|---|
| 1 | Задать Status = Pending Approval, диапазон дат, покрывающий созданные заявки |
| 2 | Нажать Search |

Expected Result:
- В таблице отображаются только заявки со статусом Pending Approval из указанного диапазона дат.
- «No Records Found» не отображается.
- Данные в строках (сотрудник, тип, даты, статус) совпадают с ожидаемыми.

Postconditions:
- Данные в системе не изменились.

### TC-LEAVE-LIST-018 — Search с комбинацией без совпадений

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Leave Type | тип, по которому заведомо нет заявок (например, US - FMLA) |
| Status | любой валидный параметр |

Preconditions:
- Пользователь авторизован.
- Открыта Leave → Leave List.

Steps:

| # | Action |
|---|---|
| 1 | Задать Leave Type, по которому нет заявок, Status — любой валидный |
| 2 | Нажать Search |

Expected Result:
- Отображается «No Records Found».
- Ошибок не возникает.

Postconditions:
- Данные в системе не изменились.

### TC-LEAVE-LIST-019 — Пустые необязательные поля не сужают результат

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| From Date / To Date | значения по умолчанию |
| Show Leave with Status | один валидный параметр |
| Leave Type | -- Select -- |
| Employee Name | пусто |
| Sub Unit | -- Select -- |
| Include Past Employees | OFF |

Preconditions:
- Пользователь авторизован.
- Открыта Leave → Leave List.
- Выполнен TC-LEAVE-LIST-001.

Steps:

| # | Action |
|---|---|
| 1 | Заполнить только обязательное поле Status, остальные поля оставить как есть |
| 2 | Нажать Search |

Expected Result:
- Поиск выполняется без ошибок.
- Результат не сужается за счёт незаполненных необязательных полей: возвращаются все записи с выбранным статусом независимо от Leave Type, Sub Unit, Employee Name и Include Past Employees.

Postconditions:
- Данные в системе не изменились.

### TC-LEAVE-LIST-020 — Комбинации фильтров (pairwise): Status × Leave Type × Sub Unit × Include Past Employees

Priority: High

Test Data:

Employee Name во всех строках оставить пустым (связь Employee Name × Sub Unit проверена отдельно в TC-LEAVE-LIST-012 и TC-LEAVE-LIST-013). From Date и To Date во всех строках — валидный диапазон, покрывающий тестовые данные (например, 2026-01-01 — 2026-12-31).

| # | Status | Leave Type | Sub Unit | Include Past Employees |
|---|---|---|---|---|
| 1 | один параметр | CAN | Finance | no |
| 2 | 5 сразу | US | Human Resources | yes |
| 3 | один параметр | US | Administration | yes |
| 4 | 5 сразу | US | Engineering | no |
| 5 | один параметр | CAN | Sales & Marketing | yes |
| 6 | один параметр | US | Client Services | yes |
| 7 | 5 сразу | CAN | Administration | no |
| 8 | 5 сразу | US | Sales & Marketing | no |
| 9 | 5 сразу | CAN | Client Services | no |
| 10 | 5 сразу | US | Finance | yes |
| 11 | один параметр | CAN | Engineering | yes |
| 12 | один параметр | CAN | Human Resources | no |

Preconditions:
- Пользователь авторизован.
- Открыта Leave → Leave List.
- Выполнен TC-LEAVE-LIST-001.

Steps:

| # | Action |
|---|---|
| 1 | Для строки 1 таблицы Test Data задать соответствующие значения полей, нажать Search |
| 2 | Зафиксировать результат |
| 3 | Нажать Reset |
| 4 | Повторить шаги 1–3 для каждой из строк 2–12 |

Expected Result:
- Для каждой строки в результатах отображаются только записи, одновременно удовлетворяющие всем заданным условиям (диапазон дат И один из выбранных статусов И выбранный Leave Type И выбранный Sub Unit И соответствие Include Past Employees).
- Если совпадений нет — отображается «No Records Found».
- Ни на одной из строк не возникает технических ошибок (500, белый экран, зависание).

Postconditions:
- Данные в системе не изменились.
