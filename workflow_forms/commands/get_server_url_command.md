---
description: Возвращает URL серверной части
---

# GetServerUrlCommand

## Шаблон GetServerUrlCommand <a href="#template" id="template"></a>

```xml
<Command Name="" Type="GetServerUrlCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для GetServerUrlCommand-->
  <Async Value="" />
</Command>
```

## Описание GetServerUrlCommand <a href="#description" id="description"></a>

```xml
<Command Name="GetServerUrlCommand" Type="GetServerUrlCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для GetServerUrlCommand-->
</Command>
```

### Результат выполнения GetServerUrlCommand <a href="#result" id="result"></a>

#### Value <a href="#result_value" id="result_value"></a>

URL серверной части.

## Тэги, специфичные для GetServerUrlCommand <a href="#specific-tags" id="specific-tags"></a>

### Async <a href="#async" id="async"></a>

Признак, определяющий, будет ли выполнение команды происходить в асинхронном режиме (в фоновом потоке).

Необязательный тэг. Значение тэга не ожидается.\
Обязательный атрибут `Value` ожидает логическое значение

По умолчанию используется значение False.

```xml
<Async Value="False" />
```
