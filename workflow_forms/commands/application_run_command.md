---
description: Команда; запускает внешнее приложение с параметрами.
---

# ApplicationRunCommand

## Шаблон ApplicationRunCommand <a href="#template" id="template"></a>

```xml
<Command Name="" Type="ApplicationRunCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для ApplicationRunCommand-->
  <Async Value="" />
  <Application></Application>
  <Arguments></Arguments>
</Command>
```

## Описание ApplicationRunCommand <a href="#description" id="description"></a>

```xml
<Command Name="ApplicationRunCommandName" Type="ApplicationRunCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для ApplicationRunCommand-->
</Command>
```

### Результат выполнения ApplicationRunCommand <a href="#result" id="result"></a>

Команда не имеет результата.

## Тэги, специфичные для ApplicationRunCommand <a href="#specific-tags" id="specific-tags"></a>

### Async <a href="#async" id="async"></a>

Признак, определяющий, будет ли выполнение команды происходить в асинхронном режиме (в фоновом потоке).

Необязательный тэг. Значение тэга не ожидается.\
Обязательный атрибут `Value` ожидает логическое значение

По умолчанию используется значение False.

```xml
<Async Value="False" />
```

### Application <a href="#application" id="application"></a>

Путь до открываемого приложения (файла).

Необязательный тэг. Любое значение будет переведено в текстовое.

Если значение тэга `<Application>` пустое, то используется значение, заданное в тэге [`<Arguments>`](application_run_command.md#arguments).

Если значение тэга [`<Arguments>`](application_run_command.md#arguments) будет также пустым, то команда ничего не выполнит.

Поддерживаются [константы замены](../values/replacement_constants.md).

```xml
<Application>Application</Application>
```

### Arguments <a href="#arguments" id="arguments"></a>

Аргументы для запуска приложения.

Необязательный тэг. Любое значение будет переведено в текстовое.

Поддерживаются [константы замены](../values/replacement_constants.md).

```xml
<Arguments>Arguments</Arguments>
```
