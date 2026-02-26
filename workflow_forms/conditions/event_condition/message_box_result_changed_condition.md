---
description: >-
  Событийное условие; срабатывает при определенном результате команды типа
  MessageBoxCommand.
---

# MessageBoxResultChangedCondition

## Шаблон MessageBoxResultChangedCondition <a href="#template_message_box_result_changed_condition" id="template_message_box_result_changed_condition"></a>

```xml
<Condition Name="" Type="MessageBoxResultChangedCondition" Assembly="Conditions">
  <!--Тэги, общие для всех условий-->
  <AlwaysChange Value="" />
  <!--Тэги, специфичные для MessageBoxResultChangedCondition-->
  <MessageBoxCommand Name="" />
  <Result Type="" />
</Condition>
```

## Описание MessageBoxResultChangedCondition <a href="#description_message_box_result_changed_condition" id="description_message_box_result_changed_condition"></a>

```xml
<Condition Name="MessageBoxResultChangedConditionName" Type="MessageBoxResultChangedCondition" Assembly="Conditions">
  <!--Тэги, общие для всех условий-->
  <!--Тэги, специфичные для MessageBoxResultChangedCondition-->
</Condition>
```

## Тэги, специфичные для MessageBoxResultChangedCondition <a href="#tags_message_box_result_changed_condition" id="tags_message_box_result_changed_condition"></a>

### MessageBoxCommand <a href="#message_box_command" id="message_box_command"></a>

Команда типа [MessageBoxCommand](../../commands/message_box_command.md), в которой срабатывает событие изменения результата.

Обязательный тэг. Значение тэга `<MessageBoxCommand>`: не ожидается.

```xml
<MessageBoxCommand Name="MessageBoxCommandName" />
```

#### Атрибуты тэга `<MessageBoxCommand>` <a href="#attributes_tag_message_box_command" id="attributes_tag_message_box_command"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="469.06057385759834"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название команды типа MessageBoxCommand.</p><p></p><p>Обязательный атрибут. Ожидается название одной из команд типа MessageBoxCommand, описанных в форме.</p></td></tr></tbody></table>

### Result <a href="#result" id="result"></a>

Результат команды типа MessageBoxCommand.

Обязательный тэг. Значение тэга `<Result>`: не ожидается.

```xml
<Result Type="ResultType" />
```

#### Атрибуты тэга `<Result>` <a href="#attributes_tag_result" id="attributes_tag_result"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="469.06057385759834"></th></tr></thead><tbody><tr><td align="center">Type</td><td><p>Тип результата (зависит от параметров самой команды).</p><p></p><p>Обязательный атрибут. Ожидается название одного из значений: OK, Cancel, Yes, No, Ignore, Retry, Abort.</p></td></tr></tbody></table>
