---
description: Команда; задает текст в статус-баре.
---

# StatusBarCommand

## Шаблон StatusBarCommand <a href="#template_status_bar_command" id="template_status_bar_command"></a>

```xml
<Command Name="" Type="StatusBarCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для StatusBarCommand-->
  <Text></Text>
</Command>
```

## Описание StatusBarCommand <a href="#description_status_bar_command" id="description_status_bar_command"></a>

```xml
<Command Name="StatusBarCommandName" Type="StatusBarCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для StatusBarCommand-->
</Command>
```

### Результат выполнения StatusBarCommand <a href="#result_status_bar_command" id="result_status_bar_command"></a>

Команда не имеет результата.

## Тэги, специфичные для StatusBarCommand <a href="#tags_status_bar_command" id="tags_status_bar_command"></a>

### Text <a href="#text" id="text"></a>

Текст для размещения в статус-баре.

Обязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Text>Текст</Text>
```
