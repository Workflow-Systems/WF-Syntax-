---
description: Команда; закрывает сеанс пользователя, перезагружает или выключает Windows.
---

# ExitWindowsCommand

## Шаблон ExitWindowsCommand <a href="#template_exit_windows_command" id="template_exit_windows_command"></a>

```xml
<Command Name="" Type="ExitWindowsCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для ExitWindowsCommand-->
  <Exit Type="" />
</Command>
```

## Описание ExitWindowsCommand <a href="#description_exit_windows_command" id="description_exit_windows_command"></a>

```xml
<Command Name="ExitWindowsCommandName" Type="ExitWindowsCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для ExitWindowsCommand-->
</Command>
```

### Результат выполнения ExitWindowsCommand <a href="#result_exit_windows_command" id="result_exit_windows_command"></a>

Команда не имеет результата.

## Тэги, специфичные для ExitWindowsCommand <a href="#tags_exit_windows_command" id="tags_exit_windows_command"></a>

### Exit <a href="#exit" id="exit"></a>

Тип закрытия Windows.

Обязательный тэг. Значение тэга `<Exit>`: не ожидается.

```xml
<Exit Type="LogOff" />
```

#### Атрибуты тэга `<Exit>` <a href="#attributes_tag_exit" id="attributes_tag_exit"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="485.92824192721685"></th></tr></thead><tbody><tr><td align="center">Type</td><td><p>Название типа закрытия Windows.</p><p></p><p>Обязательный атрибут. Ожидается название одного из <a href="exit_windows_command.md#windows_close_types">типов закрытия Windows</a>.</p></td></tr></tbody></table>

#### Типы закрытия Windows <a href="#windows_close_types" id="windows_close_types"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="485.92824192721685"></th></tr></thead><tbody><tr><td align="center">LogOff</td><td>Закрытие сеанса пользователя</td></tr><tr><td align="center">ForceLogOff</td><td>Закрытие сеанса пользователя с принудительным закрытием всех программ</td></tr><tr><td align="center">Reboot</td><td>Перезагрузка Windows</td></tr><tr><td align="center">Shutdown</td><td>Выключение Windows</td></tr></tbody></table>
