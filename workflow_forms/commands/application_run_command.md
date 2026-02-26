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

Необязательный тэг. Значение тэга `<Async>`: не ожидается.

Если тэг `<Async>` отсутствует, то для атрибута `Value` используется значение False.

```xml
<Async Value="False" />
```

#### Атрибуты тэга `<Async>` <a href="#attributes_tag_async" id="attributes_tag_async"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="476.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

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
