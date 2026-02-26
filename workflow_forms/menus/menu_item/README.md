---
description: Любой элемент меню.
---

# MenuItem

## Описание MenuItem <a href="#description" id="description"></a>

```xml
<MenuItem Name="MenuItemName" Type="MenuItemType">
  <!--Тэги, общие для всех элементов меню-->
  <!--Тэги, специфичные для определенного элемента меню (зависит от типа)-->
</MenuItem>
```

Элементы меню значения не имеют.

#### Атрибуты MenuItem <a href="#attributes_menu_item" id="attributes_menu_item"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="457.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название элемента меню.</p><p></p><p>Обязательный атрибут.</p></td></tr><tr><td align="center">Type</td><td><p>Название типа элемента меню.</p><p></p><p>Обязательный атрибут.</p></td></tr></tbody></table>

## Тэги, общие для всех элементов меню <a href="#common_tags" id="common_tags"></a>

### Enabled <a href="#enabled" id="enabled"></a>

Признак активности элемента меню.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение True.

```xml
<Enabled>True</Enabled>
```

### Visible <a href="#visible" id="visible"></a>

Признак видимости элемента меню.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение True.

```xml
<Visible>True</Visible>
```

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

Перечисленные ниже get-проперти являются общими для всех элементов меню и предназначены для получения свойств данного элемента меню.

### Enabled <a href="#get_enabled" id="get_enabled"></a>

Возвращает признак активности элемента меню.

```xml
<Object Name="MenuItemName">
  <Property Name="Enabled" />
</Object>
```

### Visible <a href="#get_visible" id="get_visible"></a>

Возвращает признак видимости элемента меню.

```xml
<Object Name="MenuItemName">
  <Property Name="Visible" />
</Object>
```

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

Перечисленные ниже set-проперти являются общими для всех элементов меню и предназначены для динамического задания свойств элемента меню (динамическое - означает, что в процессе работы формы, то есть посредством команды [`ValueSetCommand`](../../commands/value_set_command.md)).

### Enabled <a href="#set_enabled" id="set_enabled"></a>

Задает признак активности элемента меню.

Ожидается логическое значение.

```xml
<Object Name="MenuItemName">
  <Property Name="Enabled">True</Property>
</Object>
```

### Visible <a href="#set_visible" id="set_visible"></a>

Задает признак видимости элемента меню.

Ожидается логическое значение.

```xml
<Object Name="MenuItemName">
  <Property Name="Visible">True</Property>
</Object>
```
