---
description: Команда; выполняет запись значения в текстовый буфер обмена Windows.
---

# ClipboardSetCommand

## Шаблон ClipboardSetCommand <a href="#template" id="template"></a>

```xml
<Command Name="" Type="ClipboardSetCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для ClipboardSetCommand-->
  <ClipboardText></ClipboardText>
</Command>
```

## Описание ClipboardSetCommand <a href="#description" id="description"></a>

```xml
<Command Name="ClipboardSetCommandName" Type="ClipboardSetCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для ClipboardSetCommand-->
</Command>
```

### Результат выполнения ClipboardSetCommand <a href="#result" id="result"></a>

Команда не имеет результата.

## Тэги, специфичные для ClipboardSetCommand <a href="#specific-tags" id="specific-tags"></a>

### ClipboardText <a href="#clipboard_text" id="clipboard_text"></a>

Текст для записи в буфер обмена Windows.

Обязательный тэг. Любое значение будет переведено в текстовое.

```xml
<ClipboardText>текст</ClipboardText>
```
