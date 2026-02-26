---
description: Команда; показывает контекстное меню в определенной части экрана.
---

# ContextMenuShowCommand

## Шаблон ContextMenuShowCommand <a href="#template" id="template"></a>

```xml
<Command Name="" Type="ContextMenuShowCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для ContextMenuShowCommand-->
  <ContextMenu Name="" />
  <Top></Top>
  <Left></Left>
</Command>
```

## Описание ContextMenuShowCommand <a href="#description" id="description"></a>

```xml
<Command Name="ContextMenuShowCommandName" Type="ContextMenuShowCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для ContextMenuShowCommand-->
</Command>
```

### Результат выполнения ContextMenuShowCommand <a href="#result" id="result"></a>

Команда не имеет результата.

## Тэги, специфичные для ContextMenuShowCommand <a href="#specific-tags" id="specific-tags"></a>

### ContextMenu <a href="#context_menu" id="context_menu"></a>

Контекстное меню.

Обязательный тэг. Значение тэга `<ContextMenu>`: не ожидается.

```xml
<ContextMenu Name="ContextMenuName" />
```

#### Атрибуты тэга `<ContextMenu>` <a href="#attributes_tag_context_menu" id="attributes_tag_context_menu"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="496.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название контекстного меню.</p><p></p><p>Обязательный атрибут. Ожидается название одного из контекстных меню, описанных в форме.</p></td></tr></tbody></table>

### Top <a href="#top" id="top"></a>

Координата появления контекстного меню по высоте (от верхнего края формы вниз).

Необязательный тэг. Ожидается целочисленное значение.

Если тэг `<Top>` отсутствует, то используется значение 0.

```xml
<Top>0</Top>
```

### Left <a href="#left" id="left"></a>

Координата появления контекстного меню по ширине (от левого края формы направо).

Необязательный тэг. Ожидается целочисленное значение.

Если тэг `<Left>` отсутствует, то используется значение 0.

```xml
<Left>0</Left>
```
