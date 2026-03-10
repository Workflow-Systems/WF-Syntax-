---
description: Команда; присваивает фокус заданному объекту на форме.
---

# FocusSetCommand

## Шаблон FocusSetCommand <a href="#template_focus_set_command" id="template_focus_set_command"></a>

```xml
<Command Name="" Type="FocusSetCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для FocusSetCommand-->
  <Object Name="" />
</Command>
```

## Описание FocusSetCommand <a href="#description_focus_set_command" id="description_focus_set_command"></a>

```xml
<Command Name="FocusSetCommandName" Type="FocusSetCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для FocusSetCommand-->
</Command>
```

### Результат выполнения FocusSetCommand <a href="#result_focus_set_command" id="result_focus_set_command"></a>

Команда не имеет результата.

## Тэги, специфичные для FocusSetCommand <a href="#tags_focus_set_command" id="tags_focus_set_command"></a>

### Object <a href="#object" id="object"></a>

Объект, которому будет присвоен фокус.

Обязательный тэг. Значение тэга не ожидается.\
Обязательный атрибут Name ожидает название одного из объектов на форме.

```xml
<Object Name="ObjectName" />
```
