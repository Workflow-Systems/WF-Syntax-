---
description: Контекстное меню с произвольным количеством элементов.
---

# ListContextMenu

## Шаблон ListContextMenu <a href="#template" id="template"></a>

```xml
<ContextMenu Name="" Type="ListContextMenu">
  <MenuItems />
</ContextMenu>
```

## Описание ListContextMenu <a href="#description" id="description"></a>

```xml
<ContextMenu Name="ListContextMenuName" Type="ListContextMenu">
  <!--Тэги, общие для всех контекстных меню-->
  <!--Тэги, специфичные для ListContextMenu-->
</ContextMenu>
```

## Тэги, специфичные для ListContextMenu <a href="#specific-tags" id="specific-tags"></a>

### MenuItems <a href="#menu_items" id="menu_items"></a>

Список элементов.

Необязательный тэг. Ожидается таблица с четырьмя столбцами (например, ссылка на [GetDataConnection](../../dataconnections/) с указанием четырех его полей).

Первое поле будет соответствовать отображаемому заголовку элемента.

Второе - значению элемента.

Третье - всплывающей подсказке для элемента.

Четвертое - признаку активности для элемента (по умолчанию true).

Пятое - изображение, которое будет расположено на элементе меню.

Шестое - тип элемента меню: [Separator](../menu_item/menu_item_separator.md) или [MenuItem](../menu_item/menu_item_menu_item.md) (по умолчанию MenuItem).

Седьмое - Id элемента для иерархии.

Восьмое - ParentId родитель элемента для иерархии (обязательно должен быть хоть один элемент с пустым ParentId).

Можно не указывать ParentId и Id, но если указано либо то либо, то обязательно нужно присутствие обоих полей.

```xml
<MenuItems>
  <DataConnection SourceDataConnection="SourceDataConnectionName">
    <Fields>
      <Field Name="TitleFieldName" />
      <Field Name="ValueFieldName" />
      <Field Name="HintFieldName" />
      <Field Name="EnabledFieldName" />
      <Field Name="IconFieldName" />
      <Field Name="TypeFieldName" />
      <Field Name="IdFieldName" />
      <Field Name="ParentIdFieldName" />
    </Fields>
  </DataConnection>
```

### FieldOrder <a href="#field_order" id="field_order"></a>

Порядок элементов.

Необязательный тэг.

Порядковые номера по умолчанию приведены ниже. Можно написать только те поля, которые выбиваются из значений по умолчанию.

```xml
<FieldOrder>
    <Title Index="0" />
    <Value Index="1" />
    <Hint Index="2" />
    <Enabled Index="3" />
    <Icon Index="4" />
    <Type Index="5" />
    <Id Index="6" />
    <ParentId Index="7" />
  </FieldOrder>  
</MenuItems>
```

## Get-проперти для получения свойств <a href="#get_properties" id="get_properties"></a>

### ClickedMenuItemValue <a href="#get_clicked_menu_item_value" id="get_clicked_menu_item_value"></a>

Возвращает значение последнего выбранного (по которому был совершен клик мышкой) элемента.

```xml
<Object Name="ListContextMenu">
  <Property Name="ClickedMenuItemValue" />
</Object>
```

### ClickedMenuItemDisplayValue <a href="#get_clicked_menu_item_display_value" id="get_clicked_menu_item_display_value"></a>

Возвращает текст последнего выбранного (по которому был совершен клик мышкой) элемента.

```xml
<Object Name="ListContextMenu">
  <Property Name="ClickedMenuItemDisplayValue" />
</Object>
```
