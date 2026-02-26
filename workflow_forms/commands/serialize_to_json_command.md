---
description: Команда; сериализует переменную в json строку.
---

# SerializeToJsonCommand

## Шаблон SerializeToJsonCommand <a href="#template_serialize_to_json_command" id="template_serialize_to_json_command"></a>

```xml
<Command Name="" Type="SerializeToJsonCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для SerializeToJsonCommand-->
  <Async Value="" />
  <Variable></Variable>
</Command>
```

## Описание SerializeToJsonCommand <a href="#description_serialize_to_json_command" id="description_serialize_to_json_command"></a>

```xml
<Command Name="SerializeToJsonCommandName" Type="SerializeToJsonCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для SerializeToJsonCommand-->
</Command>
```

### Результат выполнения SerializeToJsonCommand <a href="#result_serialize_to_json_command" id="result_serialize_to_json_command"></a>

#### Value <a href="#result_value" id="result_value"></a>

Строка содержащая представление переменной в json.

## Тэги, специфичные для SerializeToJsonCommand <a href="#tags_serialize_to_json_command" id="tags_serialize_to_json_command"></a>

### Async <a href="#async" id="async"></a>

Признак, определяющий, будет ли выполнение команды происходить в асинхронном режиме (в фоновом потоке).

Необязательный тэг. Значение тэга `<Async>`: не ожидается.

Если тэг `<Async>` отсутствует, то для атрибута `Value` используется значение False.

```xml
<Async Value="False" />
```

#### Атрибуты тэга `<Async>` <a href="#attributes_tag_async" id="attributes_tag_async"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

### Variable <a href="#variable" id="variable"></a>

[Переменная](../objects/variable.md), которая будет сериализована в json строку.

Обязательный тэг. Значение тэга `<Variable>`: любое значение.

```xml
<Variable></Variable>
```
