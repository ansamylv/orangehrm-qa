### TC-PIM-ADD-001 — Создание сотрудника с минимальным набором полей (без логина)

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| First Name | QA_Min_01 |
| Middle Name | пусто |
| Last Name | Add |
| Create Login Details | OFF |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.

Steps:

| # | Action |
|---|---|
| 1 | Ввести First Name и Last Name |
| 2 | Выключить переключатель Create Login Details |
| 3 | Нажать Save |
| 4 | Перейти в PIM → Employee List и найти сотрудника по QA_Min_01 |

Expected Result:
- Отображается сообщение об успешном сохранении, открывается профиль сотрудника.
- Пустой Middle Name не блокирует создание (необязательное поле).
- Сотрудник присутствует в Employee List, имя совпадает с введённым.

Postconditions:
- В системе появился сотрудник QA_Min_01 Add.

### TC-PIM-ADD-002 — Создание сотрудника со всеми полями и логином

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| First Name / Middle Name / Last Name | QA_Full_01 / Middle / Add |
| Employee Id | уникальное значение (например, 9101) |
| Аватарка | avatar_ok.jpg (менее 1 МБ) |
| Create Login Details | ON |
| Username | QA_tester_001 |
| Status | Enabled |
| Password / Confirm Password | Aa1!bcde / Aa1!bcde |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.

Steps:

| # | Action |
|---|---|
| 1 | Загрузить аватарку через кнопку «+» |
| 2 | Заполнить First Name, Middle Name, Last Name |
| 3 | Заменить Employee Id на уникальное значение |
| 4 | Убедиться, что Create Login Details включён, заполнить Username, Password и Confirm Password, оставить Status = Enabled |
| 5 | Нажать Save |
| 6 | Перейти в PIM → Employee List и найти сотрудника |
| 7 | Перейти в Admin → User Management и найти пользователя по Username |

Expected Result:
- Отображается сообщение об успешном сохранении, открывается профиль сотрудника.
- Имя, Employee Id и аватарка в профиле совпадают с введёнными.
- Сотрудник присутствует в Employee List.
- Пользователь QA_tester_001 присутствует в User Management со статусом Enabled.

Postconditions:
- В системе появились сотрудник QA_Full_01 Add и пользователь QA_tester_001.

### TC-PIM-ADD-003 — Кнопка «+» открывает выбор файла аватарки

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Файл | avatar_ok.jpg (менее 1 МБ) |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.

Steps:

| # | Action |
|---|---|
| 1 | Нажать кнопку «+» на аватарке |
| 2 | Выбрать файл в диалоговом окне |

Expected Result:
- Открывается системный диалог выбора файла.
- После выбора вместо силуэта по умолчанию отображается выбранное изображение.

Postconditions:
- Сотрудник не создан.

### TC-PIM-ADD-004 — Загрузка аватарки допустимых форматов

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Файл 1 | avatar.jpg |
| Файл 2 | avatar.png |
| Файл 3 | avatar.gif |
| Размер файлов | менее 1 МБ |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.

Steps:

| # | Action |
|---|---|
| 1 | Нажать «+» и выбрать avatar.jpg |
| 2 | Зафиксировать результат |
| 3 | Повторить шаги 1–2 для avatar.png и avatar.gif |
| 4 | Заполнить First Name, Last Name (QA_Avatar_01 / Add), отключить Create Login Details и нажать Save с последним загруженным файлом |

Expected Result:
- Все три формата принимаются, сообщение об ошибке не отображается.
- Выбранное изображение отображается на месте аватарки.
- После Save аватарка отображается в профиле сотрудника.

Postconditions:
- В системе появился сотрудник QA_Avatar_01 Add.

### TC-PIM-ADD-005 — Загрузка аватарки недопустимого формата

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Файл 1 | test.pdf |
| Файл 2 | test.txt |
| Файл 3 | test.webp |
| Файл 4 | text_file.png (текстовый файл, переименованный в .png) |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.

Steps:

| # | Action |
|---|---|
| 1 | Нажать «+» и выбрать test.pdf |
| 2 | Зафиксировать результат |
| 3 | Повторить шаги 1–2 для остальных файлов |

Expected Result:
- Для каждого файла отображается сообщение об ошибке типа файла.
- Аватарка не загружена, отображается изображение по умолчанию.
- Файл text_file.png (содержимое не соответствует расширению) также отклонён с сообщением об ошибке.

Postconditions:
- Сотрудник не создан.

### TC-PIM-ADD-006 — Загрузка аватарки размером до 1 МБ включительно

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Файл 1 | avatar_500kb.jpg (около 500 КБ) |
| Файл 2 | avatar_1mb.jpg (ровно 1 МБ, 1 048 576 байт) |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.

Steps:

| # | Action |
|---|---|
| 1 | Нажать «+» и выбрать avatar_500kb.jpg |
| 2 | Зафиксировать результат |
| 3 | Нажать «+» и выбрать avatar_1mb.jpg |
| 4 | Зафиксировать результат |

Expected Result:
- Оба файла принимаются, сообщение об ошибке не отображается.

Postconditions:
- Сотрудник не создан.

### TC-PIM-ADD-007 — Загрузка аватарки размером больше 1 МБ

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Файл 1 | avatar_1mb_plus1.jpg (1 МБ + 1 байт) |
| Файл 2 | avatar_2mb.jpg (2 МБ) |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.

Steps:

| # | Action |
|---|---|
| 1 | Нажать «+» и выбрать avatar_1mb_plus1.jpg |
| 2 | Зафиксировать результат |
| 3 | Нажать «+» и выбрать avatar_2mb.jpg |
| 4 | Зафиксировать результат |

Expected Result:
- Для обоих файлов отображается сообщение о превышении допустимого размера (1 МБ).
- Аватарка не загружена, отображается изображение по умолчанию.

Postconditions:
- Сотрудник не создан.

### TC-PIM-ADD-008 — Загрузка аватарки с разными размерами изображения

Priority: Low

Test Data:

| Parameter | Value |
|---|---|
| Файл 1 | avatar_100x100.png |
| Файл 2 | avatar_200x200.png |
| Файл 3 | avatar_1000x1000.png |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.

Steps:

| # | Action |
|---|---|
| 1 | Нажать «+» и выбрать avatar_100x100.png |
| 2 | Зафиксировать результат |
| 3 | Повторить шаги 1–2 для остальных файлов |

Expected Result:
- Все три файла принимаются, сообщение об ошибке не отображается (размер 200×200 рекомендованный, а не обязательный).
- Выбранное изображение отображается на месте аватарки.

Postconditions:
- Сотрудник не создан.

### TC-PIM-ADD-009 — Допустимые значения в полях First Name, Middle Name и Last Name

Priority: High

Test Data:

| Набор | First Name | Middle Name | Last Name |
|---|---|---|---|
| 1 (латиница) | QA_John | QA_Middle | QA_Smith |
| 2 (кириллица) | Иван | Иванович | Иванов |
| 3 (1 символ) | A | B | C |
| 4 (30 символов) | A × 30 | B × 30 | C × 30 |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.

Steps:

| # | Action |
|---|---|
| 1 | Ввести значения набора 1 в First Name, Middle Name, Last Name |
| 2 | Выключить Create Login Details и нажать Save |
| 3 | Убедиться, что сотрудник создан, и данные в профиле совпадают |
| 4 | Повторить шаги 1–3 для наборов 2, 3 и 4 |

Expected Result:
- Для каждого набора отображается сообщение об успешном сохранении.
- Данные в профиле совпадают с введёнными, кириллица отображается корректно.

Postconditions:
- В системе появились 4 тестовых сотрудника.

### TC-PIM-ADD-010 — Значение в 31 символ в полях имён

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Значение | 31 символ (A × 31) |
| Проверяемое поле | First Name, Middle Name, Last Name (по очереди) |
| Остальные поля | валидны |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.

Steps:

| # | Action |
|---|---|
| 1 | Ввести 31 символ в First Name, в остальные поля ввести валидные значения |
| 2 | Нажать Save |
| 3 | Зафиксировать результат |
| 4 | Повторить шаги 1–3 для Middle Name, затем для Last Name |

Expected Result:
- Под проверяемым полем отображается сообщение об ошибке (превышена допустимая длина).
- Форма не отправляется, открыта страница Add Employee.
- Сотрудник не создан.

Postconditions:
- Данные в системе не изменились.

### TC-PIM-ADD-011 — Пустой First Name

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| First Name | пусто |
| Last Name | QA_NoFirst |
| Остальные поля | валидны |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.

Steps:

| # | Action |
|---|---|
| 1 | Оставить First Name пустым, ввести Last Name |
| 2 | Выключить Create Login Details |
| 3 | Нажать Save |
| 4 | Перейти в Employee List и найти запись по QA_NoFirst |

Expected Result:
- Под полем First Name отображается сообщение Required.
- Форма не отправляется, открыта страница Add Employee.
- Сотрудник не создан.

Postconditions:
- Данные в системе не изменились.

### TC-PIM-ADD-012 — Пустой Last Name

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| First Name | QA_NoLast |
| Last Name | пусто |
| Остальные поля | валидны |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.

Steps:

| # | Action |
|---|---|
| 1 | Ввести First Name, оставить Last Name пустым |
| 2 | Выключить Create Login Details |
| 3 | Нажать Save |
| 4 | Перейти в Employee List и найти запись по QA_NoLast |

Expected Result:
- Под полем Last Name отображается сообщение Required.
- Форма не отправляется, открыта страница Add Employee.
- Сотрудник не создан.

Postconditions:
- Данные в системе не изменились.

### TC-PIM-ADD-013 — Только пробелы в First Name и Last Name

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Значение | 3 пробела |
| Проверяемое поле | First Name, Last Name (по очереди) |
| Остальные поля | валидны |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.

Steps:

| # | Action |
|---|---|
| 1 | Ввести 3 пробела в First Name, в Last Name ввести QA_Space |
| 2 | Выключить Create Login Details и нажать Save |
| 3 | Зафиксировать результат |
| 4 | Повторить шаги 1–3 для Last Name (в First Name ввести QA_Space) |

Expected Result:
- Под проверяемым полем отображается сообщение Required (пробелы не считаются значением).
- Форма не отправляется, сотрудник не создан.

Postconditions:
- Данные в системе не изменились (удалить созданные записи, если они появились).

### TC-PIM-ADD-014 — Цифры и спецсимволы в полях имён

Priority: Low

Test Data:

| Parameter | Value |
|---|---|
| Набор 1 (цифры) | First Name: John123, Last Name: Test456 |
| Набор 2 (спецсимволы) | First Name: John!@#$%, Last Name: Test^&*() |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.

Steps:

| # | Action |
|---|---|
| 1 | Ввести значения набора 1 в First Name и Last Name |
| 2 | Выключить Create Login Details и нажать Save |
| 3 | Зафиксировать результат |
| 4 | Повторить шаги 1–3 для набора 2 |

Expected Result:
- Под полями First Name и Last Name отображается сообщение об ошибке (недопустимые символы).
- Форма не отправляется, открыта страница Add Employee.
- Сотрудник не создан.

Postconditions:
- Данные в системе не изменились.

### TC-PIM-ADD-015 — Граница длины Employee Id и очень длинное значение

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Лимит длины Employee Id | N (узнать на сайте: вводить символы до появления ошибки) |
| Значение 1 | N символов (цифры) |
| Значение 2 | N + 1 символ |
| Значение 3 | очень длинное число (30 цифр) |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.
- Определён лимит N длины Employee Id.

Steps:

| # | Action |
|---|---|
| 1 | Заменить Employee Id на значение 1, ввести First Name и Last Name |
| 2 | Выключить Create Login Details и нажать Save |
| 3 | Зафиксировать результат |
| 4 | Повторить шаги 1–3 для значений 2 и 3 |

Expected Result:
- Значение из N символов принимается, сотрудник создаётся.
- Для значений 2 и 3 под полем отображается сообщение об ошибке длины, форма не отправляется, сотрудник не создан.
- Система не выдаёт технических ошибок (500, белый экран).

Postconditions:
- В системе появился один сотрудник (со значением 1).

### TC-PIM-ADD-016 — Пустой Employee Id

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Employee Id | пусто (значение по умолчанию удалено) |
| First Name / Last Name | QA_NoId / Add |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.

Steps:

| # | Action |
|---|---|
| 1 | Удалить значение по умолчанию из поля Employee Id |
| 2 | Ввести First Name и Last Name |
| 3 | Выключить Create Login Details и нажать Save |
| 4 | Перейти в Employee List и найти запись по QA_NoId |

Expected Result:
- Под полем Employee Id отображается сообщение об ошибке (Required).
- Форма не отправляется, открыта страница Add Employee.
- Сотрудник не создан.

Postconditions:
- Данные в системе не изменились.

### TC-PIM-ADD-017 — Дубликат Employee Id

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Существующий Employee Id | 9001 (сотрудник QA_Dup_Base) |
| Новый сотрудник | QA_Dup_Id / Add |
| Employee Id нового сотрудника | 9001 |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.
- В системе существует сотрудник с Employee Id 9001 (создать заранее с именем QA_Dup_Base).

Steps:

| # | Action |
|---|---|
| 1 | Ввести First Name и Last Name нового сотрудника |
| 2 | Заменить Employee Id на 9001 |
| 3 | Выключить Create Login Details и нажать Save |
| 4 | Перейти в Employee List и найти запись по QA_Dup_Id |

Expected Result:
- Под полем Employee Id отображается сообщение о том, что значение уже существует.
- Форма не отправляется, открыта страница Add Employee.
- Второй сотрудник с Employee Id 9001 не создан.

Postconditions:
- Данные в системе не изменились (остался только QA_Dup_Base).

### TC-PIM-ADD-018 — Переключатель Create Login Details

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Username (для проверки сохранения введённых данных) | QA_Toggle_User |
| First Name / Last Name | QA_Toggle / Add |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.
- Create Login Details включён.

Steps:

| # | Action |
|---|---|
| 1 | Убедиться, что отображаются поля Username, Status, Password, Confirm Password |
| 2 | Ввести значение в Username |
| 3 | Выключить Create Login Details |
| 4 | Включить Create Login Details обратно |
| 5 | Выключить Create Login Details, ввести First Name и Last Name |
| 6 | Нажать Save |
| 7 | Перейти в Admin → User Management и найти QA_Toggle_User |

Expected Result:
- При выключении поля Username, Status, Password, Confirm Password скрываются, при включении появляются.
- При выключенном переключателе поля логина не обязательны, форма отправляется.
- Сотрудник создан без логина, пользователь QA_Toggle_User в User Management отсутствует.

Postconditions:
- В системе появился сотрудник QA_Toggle Add без логина.

### TC-PIM-ADD-019 — Допустимые значения Username

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Значение 1 | 5 символов (QA_01) |
| Значение 2 | 40 символов (латиница и цифры, уникальные) |
| First Name / Last Name | QA_UserOk / Add |
| Password / Confirm Password | Aa1!bcde / Aa1!bcde |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.
- Create Login Details включён.

Steps:

| # | Action |
|---|---|
| 1 | Ввести First Name, Last Name, Username (значение 1), Password и Confirm Password |
| 2 | Нажать Save |
| 3 | Убедиться, что сотрудник создан, и пользователь есть в Admin → User Management |
| 4 | Повторить шаги 1–3 для значения 2 (с другим именем сотрудника) |

Expected Result:
- В обоих случаях отображается сообщение об успешном сохранении.
- Пользователи с указанными Username присутствуют в User Management.

Postconditions:
- В системе появились 2 сотрудника и 2 пользователя.

### TC-PIM-ADD-020 — Недопустимая длина Username

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Значение 1 | 4 символа (QA_1) |
| Значение 2 | 41 символ |
| Остальные поля | валидны |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.
- Create Login Details включён.

Steps:

| # | Action |
|---|---|
| 1 | Заполнить остальные поля валидными значениями |
| 2 | Ввести в Username значение 1 |
| 3 | Нажать Save |
| 4 | Зафиксировать результат |
| 5 | Повторить шаги 2–4 для значения 2 |

Expected Result:
- Под полем Username отображается сообщение об ошибке длины.
- Форма не отправляется, открыта страница Add Employee.
- Сотрудник и пользователь не созданы.

Postconditions:
- Данные в системе не изменились.

### TC-PIM-ADD-021 — Пустой Username при включённом логине

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Username | пусто |
| First Name / Last Name | QA_NoUser / Add |
| Password / Confirm Password | Aa1!bcde / Aa1!bcde |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.
- Create Login Details включён.

Steps:

| # | Action |
|---|---|
| 1 | Ввести First Name, Last Name, Password и Confirm Password |
| 2 | Оставить Username пустым |
| 3 | Нажать Save |
| 4 | Перейти в Employee List и найти запись по QA_NoUser |

Expected Result:
- Под полем Username отображается сообщение Required.
- Форма не отправляется, открыта страница Add Employee.
- Сотрудник не создан.

Postconditions:
- Данные в системе не изменились.

### TC-PIM-ADD-022 — Дубликат Username

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Существующий Username | QA_Dup_User |
| Username нового сотрудника | QA_Dup_User |
| Вариант с другим регистром | qa_dup_user |
| First Name / Last Name | QA_Dup_Name / Add |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.
- В системе существует пользователь с Username QA_Dup_User (создать заранее).

Steps:

| # | Action |
|---|---|
| 1 | Ввести First Name и Last Name, оставить Employee Id уникальным |
| 2 | Ввести Username QA_Dup_User, валидные Password и Confirm Password |
| 3 | Нажать Save |
| 4 | Зафиксировать результат |
| 5 | Повторить шаги 2–4 с Username qa_dup_user |
| 6 | Перейти в Admin → User Management и найти пользователей по QA_Dup_User |

Expected Result:
- Для QA_Dup_User под полем Username отображается сообщение о том, что значение уже существует, форма не отправляется, сотрудник не создан.
- Для qa_dup_user также отображается сообщение о том, что значение уже существует, форма не отправляется, сотрудник не создан.
- В User Management нет двух пользователей с одинаковым Username.

Postconditions:
- Данные в системе не изменились (удалить лишние записи, если они появились).

### TC-PIM-ADD-023 — Кириллица, спецсимволы и пробелы в Username

Priority: Low

Test Data:

| Parameter | Value |
|---|---|
| Значение 1 (кириллица) | Юзер_QA1 |
| Значение 2 (спецсимволы) | QA@#$%1 |
| Значение 3 (пробел внутри) | QA user1 |
| Остальные поля | валидны |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.
- Create Login Details включён.

Steps:

| # | Action |
|---|---|
| 1 | Заполнить остальные поля валидными значениями |
| 2 | Ввести в Username значение 1 и нажать Save |
| 3 | Зафиксировать результат |
| 4 | Повторить шаги 2–3 для значений 2 и 3 |

Expected Result:
- Для каждого значения под полем Username отображается сообщение об ошибке (недопустимые символы или пробел).
- Форма не отправляется, открыта страница Add Employee.
- Сотрудник и пользователь не созданы.

Postconditions:
- Данные в системе не изменились.

### TC-PIM-ADD-024 — Статус Enabled и Disabled применяется после сохранения

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Сотрудник 1 | QA_Status_En / Add, Username QA_status_en, Status Enabled |
| Сотрудник 2 | QA_Status_Dis / Add, Username QA_status_dis, Status Disabled |
| Password / Confirm Password | Aa1!bcde / Aa1!bcde |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.
- Create Login Details включён.

Steps:

| # | Action |
|---|---|
| 1 | Создать сотрудника 1 со Status = Enabled |
| 2 | Создать сотрудника 2 со Status = Disabled |
| 3 | Перейти в Admin → User Management и найти пользователей по QA_status |

Expected Result:
- Оба сотрудника созданы, сообщение об успехе отображается.
- В User Management у QA_status_en статус Enabled, у QA_status_dis статус Disabled.

Postconditions:
- В системе появились 2 сотрудника и 2 пользователя.

### TC-PIM-ADD-025 — Допустимая длина Password

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Значение 1 | 7 символов (Aa1!bcd) |
| Значение 2 | 64 символа (Aa1! + a × 60) |
| Confirm Password | совпадает с Password |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.
- Create Login Details включён.
- Уточнены требования к паролю на сайте (при вводе слабого пароля форма показывает список правил), Test Data скорректированы под них.

Steps:

| # | Action |
|---|---|
| 1 | Ввести First Name, Last Name (QA_PassOk_01 / Add) и уникальный Username |
| 2 | Ввести значение 1 в Password и Confirm Password |
| 3 | Нажать Save |
| 4 | Зафиксировать результат |
| 5 | Повторить шаги 1–4 для значения 2 (с другими First Name и Username) |

Expected Result:
- В обоих случаях отображается сообщение об успешном сохранении.
- Сотрудники и пользователи созданы.

Postconditions:
- В системе появились 2 сотрудника и 2 пользователя.

### TC-PIM-ADD-026 — Недопустимая длина Password

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Значение 1 | 6 символов (Aa1!bc) |
| Значение 2 | 65 символов (Aa1! + a × 61) |
| Confirm Password | совпадает с Password |
| Остальные поля | валидны |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.
- Create Login Details включён.

Steps:

| # | Action |
|---|---|
| 1 | Заполнить остальные поля валидными значениями |
| 2 | Ввести значение 1 в Password и Confirm Password |
| 3 | Нажать Save |
| 4 | Зафиксировать результат |
| 5 | Повторить шаги 2–4 для значения 2 |

Expected Result:
- Под полем Password отображается сообщение об ошибке длины.
- Форма не отправляется, открыта страница Add Employee.
- Сотрудник и пользователь не созданы.

Postconditions:
- Данные в системе не изменились.

### TC-PIM-ADD-027 — Password без строчной буквы

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | QA1234!X (нет строчных букв, остальные правила выполнены) |
| Confirm Password | QA1234!X |
| Остальные поля | валидны |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.
- Create Login Details включён.

Steps:

| # | Action |
|---|---|
| 1 | Заполнить остальные поля валидными значениями |
| 2 | Ввести значение в Password и Confirm Password |
| 3 | Нажать Save |

Expected Result:
- Под полем Password отображается сообщение о том, что нужна строчная буква.
- Форма не отправляется, сотрудник и пользователь не созданы.

Postconditions:
- Данные в системе не изменились.

### TC-PIM-ADD-028 — Password без цифры

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Password | Qwerty!x (нет цифр, остальные правила выполнены) |
| Confirm Password | Qwerty!x |
| Остальные поля | валидны |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.
- Create Login Details включён.

Steps:

| # | Action |
|---|---|
| 1 | Заполнить остальные поля валидными значениями |
| 2 | Ввести значение в Password и Confirm Password |
| 3 | Нажать Save |

Expected Result:
- Под полем Password отображается сообщение о том, что нужна цифра.
- Форма не отправляется, сотрудник и пользователь не созданы.

Postconditions:
- Данные в системе не изменились.

### TC-PIM-ADD-029 — Confirm Password не совпадает с Password и пустой Confirm Password

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Password | Aa1!bcde |
| Confirm Password (вариант 1) | Aa1!bcdX |
| Confirm Password (вариант 2) | пусто |
| Остальные поля | валидны |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.
- Create Login Details включён.

Steps:

| # | Action |
|---|---|
| 1 | Заполнить остальные поля валидными значениями |
| 2 | Ввести Password и Confirm Password (вариант 1) |
| 3 | Нажать Save |
| 4 | Зафиксировать результат |
| 5 | Очистить Confirm Password (вариант 2) и нажать Save |
| 6 | Зафиксировать результат |

Expected Result:
- Для варианта 1 под полем Confirm Password отображается сообщение о несовпадении паролей.
- Для варианта 2 под полем Confirm Password отображается сообщение Required или о несовпадении.
- Форма не отправляется, сотрудник и пользователь не созданы.

Postconditions:
- Данные в системе не изменились.

### TC-PIM-ADD-030 — Save с несколькими невалидными полями

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| First Name | пусто |
| Last Name | пусто |
| Username | QA_1 (4 символа) |
| Password | Aa1!bc (6 символов) |
| Confirm Password | Aa1!bX (не совпадает) |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Add Employee.
- Create Login Details включён.

Steps:

| # | Action |
|---|---|
| 1 | Ввести указанные значения в поля |
| 2 | Нажать Save |
| 3 | Перейти в Employee List и проверить, что новые записи не появились |

Expected Result:
- Ошибки отображаются под всеми невалидными полями, а не только под первым.
- Форма не отправляется, открыта страница Add Employee.
- Сотрудник и пользователь не созданы.

Postconditions:
- Данные в системе не изменились.
