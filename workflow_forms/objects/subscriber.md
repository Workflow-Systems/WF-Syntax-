---
description: Объект; не имеет графического отображения.
---

# Subscriber

## Шаблон Subscriber <a href="#template" id="template"></a>

```xml
<MyObject Name="" Type="Subscriber" Assembly="SimpleControls">
  <Subscribes>
    <Subscribe></Subscribe>
  </Subscribes>
</MyObject>
```

## Описание Subscriber <a href="#description" id="description"></a>

```xml
<MyObject Name="" Type="Subscriber" Assembly="SimpleControls">
  <!--Тэги, специфичные для Subscriber-->
</MyObject>
```

## Атрибуты объекта Subscriber <a href="#attributes_subscriber" id="attributes_subscriber"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="392.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название переменной.</p><p>Обязательный атрибут.</p></td></tr><tr><td align="center">Type</td><td><p>Название типа переменной в сборке.</p><p>Обязательный атрибут.</p></td></tr><tr><td align="center">Assembly</td><td><p>Название сборки (библиотека).</p><p>Обязательный атрибут.</p></td></tr></tbody></table>

## Тэги, специфичные для Subscriber <a href="#specific-tags" id="specific-tags"></a>

### Subscribes <a href="#subscribes" id="subscribes"></a>

Список подписок

Необязательный тэг. Ожидается список тэгов [`<Subscribe>`](subscriber.md#items_item).

```xml
<Subscribes>
  <Subscribe>Subscribe1</Subscribe>
  <Subscribe>Subscribe2</Subscribe>
</Subscribes>
```

#### Тэг `<Subscribe>` <a href="#items_item" id="items_item"></a>

Название подписки.

Необязательный тэг. Любое значение будет преобразовано в текстовое.

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### Subscribe <a href="#get_subscribe" id="get_subscribe"></a>

Возвращает название события последнего принятого сообщения.

```xml
<Object Name="VariableName">
  <Property Name="Subscribe" />
</Object>
```

### Parameter <a href="#get_parameter" id="get_parameter"></a>

Возвращает значение параметра последнего принятого сообщения.

Значение тэга Property: название параметра последнего принятого сообщения.

```xml
<Object Name="VariableName">
  <Property Name="Parameter">Name</Property>
</Object>
```
