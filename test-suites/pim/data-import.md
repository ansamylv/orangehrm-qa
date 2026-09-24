### TC-PIM-IMP-001 — Импорт файла Sample CSV без изменений

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Файл | Sample CSV, скачанный по ссылке Download |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration → Data Import.

Steps:

| # | Action |
|---|---|
| 1 | Нажать Download в примечании "Sample CSV file" |
| 2 | Нажать Browse и выбрать скачанный файл |
| 3 | Нажать Upload |
| 4 | Перейти в PIM → Employee List |

Expected Result:
- Файл скачивается и открывается как CSV.
- Отображается сообщение об успешном импорте.
- Сотрудники из файла отображаются в Employee List, данные совпадают с файлом.

Postconditions:
- В системе появились импортированные сотрудники.

### TC-PIM-IMP-002 — Импорт собственного валидного CSV-файла

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Записей в файле | 3 |
| First Name / Last Name | QA_Test_01 / Import, QA_Test_02 / Import, QA_Test_03 / Import |
| Даты | YYYY-MM-DD |
| Gender | Male, Female, пусто |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration → Data Import.
- Подготовлен CSV на основе Sample CSV (порядок колонок сохранён).

Steps:

| # | Action |
|---|---|
| 1 | Нажать Browse и выбрать подготовленный файл |
| 2 | Нажать Upload |
| 3 | Перейти в PIM → Employee List и найти сотрудников по имени QA_Test |

Expected Result:
- Отображается сообщение об успешном импорте.
- Все 3 сотрудника присутствуют в Employee List с корректными данными.
- Запись с пустым Gender импортирована (необязательное поле).

Postconditions:
- В системе появились 3 тестовые записи.

### TC-PIM-IMP-003 — Нажатие Upload без выбранного файла

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Файл | не выбран |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration → Data Import.
- Поле Select File показывает "No file selected".

Steps:

| # | Action |
|---|---|
| 1 | Нажать Upload |

Expected Result:
- Под полем Select File отображается сообщение об обязательности поля (Required).
- Импорт не запускается.

Postconditions:
- Данные в системе не изменились.

### TC-PIM-IMP-004 — Загрузка файла не CSV-формата

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Файл | test.txt (или .xlsx) |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration → Data Import.
- Подготовлен файл формата, отличного от CSV.

Steps:

| # | Action |
|---|---|
| 1 | Нажать Browse и выбрать файл test.txt |
| 2 | Нажать Upload |

Expected Result:
- Файл отклонён, отображается сообщение об ошибке типа файла.
- Сотрудники не импортированы.

Postconditions:
- Данные в системе не изменились.

### TC-PIM-IMP-005 — Загрузка файла размером больше 1 МБ

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Файл | CSV размером более 1 МБ (валидная структура, поле First Name раздуто длинными значениями или файл с большим количеством пустых строк) |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration → Data Import.
- Подготовлен CSV размером > 1 МБ.

Steps:

| # | Action |
|---|---|
| 1 | Нажать Browse и выбрать файл |
| 2 | Нажать Upload |

Expected Result:
- Файл отклонён, отображается сообщение о превышении допустимого размера (1 МБ).
- Сотрудники не импортированы.

Postconditions:
- Данные в системе не изменились.

### TC-PIM-IMP-006 — Пустой First Name

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| First Name | пусто |
| Last Name | Import_QA |
| Остальные условия | выполнены |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration → Data Import.
- Подготовлен CSV с одной записью, в которой First Name пустой.

Steps:

| # | Action |
|---|---|
| 1 | Нажать Browse и выбрать файл |
| 2 | Нажать Upload |
| 3 | Перейти в Employee List и найти запись по Last Name Import_QA |

Expected Result:
- Отображается сообщение об ошибке импорта.
- Запись не создана.

Postconditions:
- Данные в системе не изменились.

### TC-PIM-IMP-007 — Пустой Last Name

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| First Name | QA_Test_LN |
| Last Name | пусто |
| Остальные условия | выполнены |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration → Data Import.
- Подготовлен CSV с одной записью, в которой Last Name пустой.

Steps:

| # | Action |
|---|---|
| 1 | Нажать Browse и выбрать файл |
| 2 | Нажать Upload |
| 3 | Перейти в Employee List и найти запись по First Name QA_Test_LN |

Expected Result:
- Отображается сообщение об ошибке импорта.
- Запись не создана.

Postconditions:
- Данные в системе не изменились.

### TC-PIM-IMP-008 — Дата в неверном формате

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Поле даты (например, Date of Birth) | 24-09-1990 |
| First Name / Last Name | QA_Test_Date / Import |
| Остальные условия | выполнены |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration → Data Import.
- Подготовлен CSV с одной записью, в которой дата указана не в формате YYYY-MM-DD.

Steps:

| # | Action |
|---|---|
| 1 | Нажать Browse и выбрать файл |
| 2 | Нажать Upload |
| 3 | Перейти в Employee List и найти запись по QA_Test_Date |

Expected Result:
- Отображается сообщение об ошибке импорта.
- Запись не создана (либо создана без даты, зафиксировать фактическое поведение).

Postconditions:
- Данные в системе не изменились.

### TC-PIM-IMP-009 — Недопустимое значение Gender

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Gender | Other |
| First Name / Last Name | QA_Test_Gender / Import |
| Остальные условия | выполнены |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration → Data Import.
- Подготовлен CSV с одной записью, в которой Gender = Other.

Steps:

| # | Action |
|---|---|
| 1 | Нажать Browse и выбрать файл |
| 2 | Нажать Upload |
| 3 | Перейти в Employee List и найти запись по QA_Test_Gender |

Expected Result:
- Отображается сообщение об ошибке импорта.
- Запись не создана.

Postconditions:
- Данные в системе не изменились.

### TC-PIM-IMP-010 — Изменён порядок колонок

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Файл | Sample CSV, в котором поменяны местами колонки First Name и Last Name |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration → Data Import.
- Подготовлен CSV с изменённым порядком колонок.

Steps:

| # | Action |
|---|---|
| 1 | Нажать Browse и выбрать файл |
| 2 | Нажать Upload |
| 3 | Перейти в Employee List и проверить импортированные записи |

Expected Result:
- Импорт отклонён с сообщением об ошибке, либо данные импортированы в перепутанные поля. Зафиксировать фактическое поведение: по требованию порядок колонок менять нельзя.

Postconditions:
- Записи, созданные с перепутанными данными, удалены.

### TC-PIM-IMP-011 — Импорт ровно 100 записей (граница)

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Записей в файле | 100 |
| Имена | QA_Bulk_001 … QA_Bulk_100 / Import |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration → Data Import.
- Подготовлен валидный CSV со 100 записями.

Steps:

| # | Action |
|---|---|
| 1 | Нажать Browse и выбрать файл |
| 2 | Нажать Upload |
| 3 | Перейти в Employee List и найти записи по QA_Bulk |

Expected Result:
- Отображается сообщение об успешном импорте.
- Все 100 записей присутствуют в Employee List.

Postconditions:
- В системе появились 100 тестовых записей.

### TC-PIM-IMP-012 — Импорт 101 записи (превышение границы)

Priority: High

Test Data:

| Parameter | Value |
|---|---|
| Записей в файле | 101 |
| Имена | QA_Over_001 … QA_Over_101 / Import |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration → Data Import.
- Подготовлен валидный CSV со 101 записью.

Steps:

| # | Action |
|---|---|
| 1 | Нажать Browse и выбрать файл |
| 2 | Нажать Upload |
| 3 | Перейти в Employee List и найти записи по QA_Over |

Expected Result:
- Отображается сообщение об ошибке (превышен лимит записей).
- Записи не импортированы (либо импортированы частично, зафиксировать фактическое поведение).

Postconditions:
- Данные в системе не изменились.

### TC-PIM-IMP-013 — Пустой файл и файл только с заголовком

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Файл 1 | пустой CSV (0 байт) |
| Файл 2 | CSV только со строкой заголовков |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration → Data Import.
- Подготовлены оба файла.

Steps:

| # | Action |
|---|---|
| 1 | Загрузить файл 1 (Browse → Upload) |
| 2 | Зафиксировать результат |
| 3 | Загрузить файл 2 (Browse → Upload) |
| 4 | Зафиксировать результат |

Expected Result:
- Для обоих файлов отображается сообщение об ошибке или о нулевом числе импортированных записей.
- Система не выдаёт технических ошибок (500, белый экран).

Postconditions:
- Данные в системе не изменились.

### TC-PIM-IMP-014 — Кнопка Browse и отображение имени файла

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Файл | валидный CSV из TC-PIM-IMP-002 |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration → Data Import.
- Поле Select File показывает "No file selected".

Steps:

| # | Action |
|---|---|
| 1 | Нажать Browse |
| 2 | Выбрать файл в диалоговом окне |

Expected Result:
- Открывается системный диалог выбора файла.
- После выбора вместо "No file selected" отображается имя файла.

Postconditions:
- Файл выбран, импорт не запущен.

### TC-PIM-IMP-015 — Кнопка со стрелкой в поле Select File

Priority: Low

Test Data:

| Parameter | Value |
|---|---|
| Файл | валидный CSV из TC-PIM-IMP-002 |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration → Data Import.
- Поле Select File показывает "No file selected".

Steps:

| # | Action |
|---|---|
| 1 | Нажать на иконку со стрелкой справа в поле Select File |
| 2 | Выбрать файл в диалоговом окне (если оно открылось) |

Expected Result:
- Иконка открывает диалог выбора файла, как кнопка Browse, и имя выбранного файла отображается в поле.
- Если иконка декоративная, зафиксировать это.

Postconditions:
- Файл выбран, импорт не запущен.

### TC-PIM-IMP-016 — Повторная загрузка валидного файла после ошибки

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Файл 1 | невалидный (пустой First Name) |
| Файл 2 | валидный CSV, записи QA_Retry_01 / Import |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration → Data Import.
- Подготовлены оба файла.

Steps:

| # | Action |
|---|---|
| 1 | Загрузить файл 1 (Browse → Upload), убедиться, что показана ошибка |
| 2 | Без перезагрузки страницы выбрать файл 2 через Browse |
| 3 | Нажать Upload |
| 4 | Перейти в Employee List и найти QA_Retry_01 |

Expected Result:
- После ошибки форма остаётся рабочей.
- Файл 2 импортирован успешно, старое сообщение об ошибке не отображается.

Postconditions:
- В системе появилась запись QA_Retry_01.

### TC-PIM-IMP-017 — Ошибка в одной строке из нескольких

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Записей в файле | 5 |
| Невалидная запись | 3-я (пустой Last Name) |
| Имена | QA_Mix_01 … QA_Mix_05 |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration → Data Import.
- Подготовлен CSV из 5 записей, одна из которых невалидна.

Steps:

| # | Action |
|---|---|
| 1 | Нажать Browse и выбрать файл |
| 2 | Нажать Upload |
| 3 | Перейти в Employee List и найти записи по QA_Mix |

Expected Result:
- Отображается сообщение об ошибке с указанием проблемной строки (или общее).
- Зафиксировать фактическое поведение: импортируются ли 4 валидные записи или не импортируется ни одной.

Postconditions:
- Удалить импортированные записи QA_Mix, если они появились.
