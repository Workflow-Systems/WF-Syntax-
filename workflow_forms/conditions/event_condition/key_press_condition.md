---
description: >-
  Событийное условие; срабатывает при нажатии клавиши символа на объекте или
  форме.
---

# KeyPressCondition

## Шаблон KeyPressCondition <a href="#template_key_press_condition" id="template_key_press_condition"></a>

```xml
<Condition Name="" Type="KeyPressCondition" Assembly="Conditions">
  <!--Тэги, общие для всех условий-->
  <AlwaysChange Value="" />
  <!--Тэги, специфичные для KeyPressCondition-->
  <Object Name="" />
  <ExceptObjects>
    <Object Name="" />
  </ExceptObjects>
  <Key Code="" />
  <Handle></Handle>
</Condition>
```

## Описание KeyPressCondition <a href="#description_key_press_condition" id="description_key_press_condition"></a>

```xml
<Condition Name="KeyPressConditionName" Type="KeyPressCondition" Assembly="Conditions">
  <!--Тэги, общие для всех условий-->
  <!--Тэги, специфичные для KeyPressCondition-->
</Condition>
```

## Тэги, специфичные для KeyPressCondition <a href="#tags_key_press_condition" id="tags_key_press_condition"></a>

### Object <a href="#object" id="object"></a>

[Объект](../../objects/), на котором срабатывает событие нажатия клавиши символа.

Необязательный тэг. Значение тэга `<Object>`: не ожидается.

Если тэг `<Object>` отсутствует, то событие срабатывает для формы.

```xml
<Object Name="ObjectName" />
```

#### Атрибуты тэга `<Object>` <a href="#attributes_tag_object" id="attributes_tag_object"></a>

<table data-header-hidden><thead><tr><th width="150" align="center"></th><th width="502.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название объекта.</p><p></p><p>Обязательный атрибут. Ожидается название одного из объектов, описанных в форме.</p></td></tr></tbody></table>

### ExceptObjects <a href="#except_objects" id="except_objects"></a>

Список [объектов](../../objects/) формы, нажатие клавиш в которых не вызывает срабатывание события.

Необязательный тэг. Значение тэга `<ExceptObjects>`: список тэгов [`<Object>`](key_press_condition.md#except_objects_object).

При наличии тэга [`<Object>`](key_press_condition.md#object) тэг `<ExceptObjects>` игнорируется.

```xml
<ExceptObjects>
  <Object Name="ObjectName1" />
  <Object Name="ObjectName2" />
</ExceptObjects>
```

#### Тэг `<Object>` <a href="#except_objects_object" id="except_objects_object"></a>

[Объект](../../objects/) формы, нажатие клавиши в котором не будет вызывать событие.

Необязательный тэг. Значение тэга `<Object>`: не ожидается.

#### Атрибуты тэга `<Object>` <a href="#attributes_tag_except_objects_object" id="attributes_tag_except_objects_object"></a>

<table data-header-hidden><thead><tr><th width="150" align="center"></th><th width="502.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название объекта.</p><p></p><p>Обязательный атрибут. Ожидается название одного из объектов, описанных в форме.</p></td></tr></tbody></table>

### Key <a href="#key" id="key"></a>

Описание нажатой клавиши.

Обязательный тэг. Значение тэга `<Key>`: не ожидается.

```xml
<Key Code="13" />
```

#### Атрибуты тэга `<Key>` <a href="#attributes_tag_key" id="attributes_tag_key"></a>

<table data-header-hidden><thead><tr><th width="150" align="center"></th><th width="502.3333333333333"></th></tr></thead><tbody><tr><td align="center">Code</td><td><p>Код нажатой клавиши.</p><p></p><p>Обязательный атрибут. Ожидается целочисленное значение от 0 до 255.</p></td></tr></tbody></table>

### Handle <a href="#handle" id="handle"></a>

Признак, определяющий, будет ли передаваться дальше на объекты управление после обработки данного условия нажатие клавиши.

Необязательный тэг. Ожидается логическое значение.

Если тэг `<Handle>` отсутствует, то используется значение True.

```xml
<Handle>True</Handle>
```
