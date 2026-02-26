---
description: Команда; печатает графическое отображение объекта со всем его содержимым.
---

# ObjectPrintCommand

## Шаблон ObjectPrintCommand <a href="#template_object_print_command" id="template_object_print_command"></a>

```xml
<Command Name="" Type="ObjectPrintCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для ObjectPrintCommand-->
  <Object Name="" />
  <ScaleRatio></ScaleRatio>
  <LandscapeOrientation></LandscapeOrientation>
</Command>
```

## Описание ObjectPrintCommand <a href="#description_object_print_command" id="description_object_print_command"></a>

```xml
<Command Name="ObjectPrintCommandName" Type="ObjectPrintCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для ObjectPrintCommand-->
</Command>
```

### Результат выполнения ObjectPrintCommand <a href="#result_object_print_command" id="result_object_print_command"></a>

Команда не имеет результата.

## Тэги, специфичные для ObjectPrintCommand <a href="#tags_object_print_command" id="tags_object_print_command"></a>

### Object <a href="#object" id="object"></a>

Объект для печати.

Обязательный тэг. Значение тэга `<Object>`: не ожидается.

```xml
<Object Name="ObjectName" />
```

#### Атрибуты тэга `<Object>` <a href="#attributes_tag_object" id="attributes_tag_object"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="464.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название одного из <a href="../objects/">объектов</a>, описанных в форме.</p><p></p><p>Обязательный атрибут. Ожидается название одного из объектов, описанных в форме.</p></td></tr></tbody></table>

### ScaleRatio <a href="#scale_ratio" id="scale_ratio"></a>

Коэффициент масштабирования выводимого на печать изображения.

Необязательный тэг. Ожидается числовое значение.

Если значение тэга `<ScaleRatio>` пустое, то используется значение 1.

```xml
<ScaleRatio>0.5</ScaleRatio>
```

### LandscapeOrientation <a href="#landscape_orientation" id="landscape_orientation"></a>

Признак, определяющий, следует ли по умолчанию горизонтально расположить лист для печати.

Необязательный тэг. Ожидается логическое значение.

Если значение тэга `<LandscapeOrientation>` пустое, то используется значение False.

```xml
<LandscapeOrientation>True</LandscapeOrientation>
```
