### TC-PIM-001 — Отображение Nickname, Military Service и Smoker при включении настройки

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Show Nick Name, Smoker and Military Service in Personal Details | ON |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration.
- Переключатель Show Nick Name, Smoker and Military Service in Personal Details находится в состоянии OFF.

Steps:

| # | Action |
|---|---|
| 1 | Включить Show Nick Name, Smoker and Military Service in Personal Details |
| 2 | Нажать Save |
| 3 | Перейти в PIM → Employee List |
| 4 | Открыть любого сотрудника |
| 5 | Открыть Personal Details |

Expected Result:
- В Personal Details отображаются поля Nickname, Military Service и Smoker.

Postconditions:
- Show Nick Name, Smoker and Military Service in Personal Details находится в состоянии ON.

### TC-PIM-002 — Скрытие Nickname, Military Service и Smoker при выключении настройки

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Show Nick Name, Smoker and Military Service in Personal Details | OFF |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration.
- Переключатель Show Nick Name, Smoker and Military Service in Personal Details находится в состоянии ON.

Steps:

| # | Action |
|---|---|
| 1 | Выключить Show Nick Name, Smoker and Military Service in Personal Details |
| 2 | Нажать Save |
| 3 | Перейти в PIM → Employee List |
| 4 | Открыть любого сотрудника |
| 5 | Открыть Personal Details |

Expected Result:
- Поля Nickname, Military Service и Smoker не отображаются в Personal Details.

Postconditions:
- Show Nick Name, Smoker and Military Service in Personal Details находится в состоянии OFF.

### TC-PIM-003 — Отображение SSN при включении настройки

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Show SSN field in Personal Details | ON |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration.
- Show SSN field in Personal Details находится в состоянии OFF.

Steps:

| # | Action |
|---|---|
| 1 | Включить Show SSN field in Personal Details |
| 2 | Нажать Save |
| 3 | Перейти в PIM → Employee List |
| 4 | Открыть любого сотрудника |
| 5 | Открыть Personal Details |

Expected Result:
- В Personal Details отображается поле SSN.

Postconditions:
- Show SSN field in Personal Details находится в состоянии ON.

### TC-PIM-004 — Скрытие SSN при выключении настройки

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Show SSN field in Personal Details | OFF |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration.
- Show SSN field in Personal Details находится в состоянии ON.

Steps:

| # | Action |
|---|---|
| 1 | Выключить Show SSN field in Personal Details |
| 2 | Нажать Save |
| 3 | Перейти в PIM → Employee List |
| 4 | Открыть любого сотрудника |
| 5 | Открыть Personal Details |

Expected Result:
- Поле SSN не отображается в Personal Details.

Postconditions:
- Show SSN field in Personal Details находится в состоянии OFF.

### TC-PIM-005 — Отображение SIN при включении настройки

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Show SIN field in Personal Details | ON |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration.
- Show SIN field in Personal Details находится в состоянии OFF.

Steps:

| # | Action |
|---|---|
| 1 | Включить Show SIN field in Personal Details |
| 2 | Нажать Save |
| 3 | Перейти в PIM → Employee List |
| 4 | Открыть любого сотрудника |
| 5 | Открыть Personal Details |

Expected Result:
- В Personal Details отображается поле SIN.

Postconditions:
- Show SIN field in Personal Details находится в состоянии ON.

### TC-PIM-006 — Скрытие SIN при выключении настройки

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Show SIN field in Personal Details | OFF |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration.
- Show SIN field in Personal Details находится в состоянии ON.

Steps:

| # | Action |
|---|---|
| 1 | Выключить Show SIN field in Personal Details |
| 2 | Нажать Save |
| 3 | Перейти в PIM → Employee List |
| 4 | Открыть любого сотрудника |
| 5 | Открыть Personal Details |

Expected Result:
- Поле SIN не отображается в Personal Details.

Postconditions:
- Show SIN field in Personal Details находится в состоянии OFF.

### TC-PIM-007 — Отображение US Tax Exemptions при включении настройки

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Show US Tax Exemptions menu | ON |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration.
- Show US Tax Exemptions menu находится в состоянии OFF.

Steps:

| # | Action |
|---|---|
| 1 | Включить Show US Tax Exemptions menu |
| 2 | Нажать Save |
| 3 | Перейти в PIM → Employee List |
| 4 | Открыть любого сотрудника |
| 5 | Проверить доступные разделы Employee |

Expected Result:
- Раздел US Tax Exemptions отображается в соответствии с включённой настройкой.

Postconditions:
- Show US Tax Exemptions menu находится в состоянии ON.

### TC-PIM-008 — Скрытие US Tax Exemptions при выключении настройки

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Show US Tax Exemptions menu | OFF |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration.
- Show US Tax Exemptions menu находится в состоянии ON.

Steps:

| # | Action |
|---|---|
| 1 | Выключить Show US Tax Exemptions menu |
| 2 | Нажать Save |
| 3 | Перейти в PIM → Employee List |
| 4 | Открыть любого сотрудника |
| 5 | Проверить доступные разделы Employee |

Expected Result:
- Раздел US Tax Exemptions не отображается в соответствии с выключенной настройкой.

Postconditions:
- Show US Tax Exemptions menu находится в состоянии OFF.

### TC-PIM-009 — Сохранение состояния Optional Fields после перезагрузки страницы

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Show Nick Name, Smoker and Military Service in Personal Details | ON |
| Show SSN field in Personal Details | ON |
| Show SIN field in Personal Details | ON |
| Show US Tax Exemptions menu | OFF |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration.

Steps:

| # | Action |
|---|---|
| 1 | Установить указанные состояния переключателей |
| 2 | Нажать Save |
| 3 | Перезагрузить страницу |

Expected Result:
- После перезагрузки все переключатели сохраняют установленные состояния.

### TC-PIM-010 — Совместная работа Optional Fields

Priority: Medium

Test Data:

| Parameter | Value |
|---|---|
| Show Nick Name, Smoker and Military Service in Personal Details | ON |
| Show SSN field in Personal Details | ON |
| Show SIN field in Personal Details | ON |
| Show US Tax Exemptions menu | OFF |

Preconditions:
- Пользователь авторизован.
- Открыта PIM → Configuration.

Steps:

| # | Action |
|---|---|
| 1 | Установить указанные состояния переключателей |
| 2 | Нажать Save |
| 3 | Перейти в PIM → Employee List |
| 4 | Открыть любого сотрудника |
| 5 | Открыть Personal Details |
| 6 | Проверить отображение дополнительных полей |

Expected Result:
- В Personal Details отображаются Nickname, Military Service, Smoker, SSN и SIN.
- Состояние одного переключателя не приводит к неожиданному изменению остальных переключателей.
