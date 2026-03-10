---
description: Возвращает информацию о резервном копировании
---

# GetCloudBackupInfoCommand

## Шаблон GetCloudBackupInfoCommand <a href="#template" id="template"></a>

```xml
<Command Name="" Type="GetCloudBackupInfoCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для GetServerUrlCommand-->
  <Async Value="" />
</Command>
```

## Описание GetCloudBackupInfoCommand <a href="#description" id="description"></a>

```xml
<Command Name="GetCloudBackupInfoCommand" Type="GetCloudBackupInfoCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для GetServerUrlCommand-->
</Command>
```

### Результат выполнения GetCloudBackupInfoCommand <a href="#result" id="result"></a>

Возвращает словарь значений:

<table data-header-hidden><thead><tr><th width="276"></th><th></th></tr></thead><tbody><tr><td>CloudBackupEnabled</td><td>Признак включено или отключено резервное копирование. Логическое значение</td></tr><tr><td>CloudBackupAvailableSpaceInGB</td><td>Доступный объем в ГБ. Дробное значение</td></tr><tr><td>CloudBackupTotalSpaceInGB</td><td>Полный объем в ГБ. Дробное значение</td></tr><tr><td>CloudBackupPath</td><td>Путь до резервных копий.</td></tr></tbody></table>

## Тэги, специфичные для GetCloudBackupInfoCommand <a href="#specific-tags" id="specific-tags"></a>

### Async <a href="#async" id="async"></a>

Признак, определяющий, будет ли выполнение команды происходить в асинхронном режиме (в фоновом потоке).

Необязательный тэг. Значение тэга не ожидается.\
Обязательный атрибут `Value` ожидает логическое значение

По умолчанию используется значение False.

```xml
<Async Value="False" />
```
