---
description: Контекстное меню с объектами - ссылками на файлы, хранящимися на сервере.
---

# FileContextMenu

## Шаблон FileContextMenu <a href="#template" id="template"></a>

```xml
<ContextMenu Name="" Type="FileContextMenu">
  <MenuItems />
</ContextMenu>
```

## Описание FileContextMenu <a href="#description" id="description"></a>

```xml
<ContextMenu Name="FileContextMenuName" Type="FileContextMenu">
  <!--Тэги, общие для всех контекстных меню-->
  <!--Тэги, специфичные для FileContextMenu-->
</ContextMenu>
```

## Тэги, специфичные для FileContextMenu <a href="#specific-tags" id="specific-tags"></a>

### MenuItems <a href="#menu_items" id="menu_items"></a>

Список ссылок.

Необязательный тэг. Ожидается таблица с четырьмя (или пятью) столбцами (например, ссылка на [GetDataConnection](../../dataconnections/) с указанием четырех или пяти его полей).

Первое поле будет соответствовать отображаемому заголовку файла.

Второе - Guid файла.

Третье - всплывающей подсказке для элемента-ссылки.

Четвертое - признаку активности для элемента-ссылки.

Пятое - признаку, можно ли отдельно сохранить файл, соответствующий элементу-ссылке.

При отсутствии поля используется значение True.

```xml
<MenuItems>
  <DataConnection SourceDataConnection="SourceDataConnectionName">
    <Fields>
      <Field Name="FileTitleFieldName" />
      <Field Name="FileGuidFieldName" />
      <Field Name="HintFieldName" />
      <Field Name="EnabledFieldName" />
      <Field Name="SaveAsFieldName" />
    </Fields>
  </DataConnection>
</MenuItems>
```

## Get-проперти для получения свойств <a href="#get_properties" id="get_properties"></a>

### ClickedMenuItemValue <a href="#get_clicked_menu_item_value" id="get_clicked_menu_item_value"></a>

Возвращает Guid-файла, соответствующего последнему выбранному (по которому был совершен клик мышкой) элементу.

```xml
<Object Name="FileContextMenu">
  <Property Name="ClickedMenuItemValue" />
</Object>
```

### ClickedMenuItemDisplayValue <a href="#get_clicked_menu_item_display_value" id="get_clicked_menu_item_display_value"></a>

Возвращает текст последнего выбранного (по которому был совершен клик мышкой) элемента.

```xml
<Object Name="FileContextMenu">
  <Property Name="ClickedMenuItemDisplayValue" />
</Object>
```
