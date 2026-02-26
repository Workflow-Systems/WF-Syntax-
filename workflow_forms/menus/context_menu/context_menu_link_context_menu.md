---
description: Контекстное меню с объектами-ссылками.
---

# LinkContextMenu

## Шаблон LinkContextMenu <a href="#template" id="template"></a>

```xml
<ContextMenu Name="" Type="LinkContextMenu">
  <MenuItems />
  <WaitWhileOpen></WaitWhileOpen>
</ContextMenu>
```

## Описание LinkContextMenu <a href="#description" id="description"></a>

```xml
<ContextMenu Name="LinkContextMenuName" Type="LinkContextMenu">
  <!--Тэги, общие для всех контекстных меню-->
  <!--Тэги, специфичные для LinkContextMenu-->
</ContextMenu>
```

## Тэги, специфичные для LinkContextMenu <a href="#specific-tags" id="specific-tags"></a>

### MenuItems <a href="#menu_items" id="menu_items"></a>

Список ссылок.

Необязательный тэг. Ожидается таблица с пятью столбцами (например, ссылка на [GetDataConnection](../../dataconnections/) с указанием пяти его полей).

Первое поле будет соответствовать отображаемому заголовку элемента-ссылки.

Второе - реальной ссылке.

Третье - приложению для запуска этой ссылки (для использования приложения по умолчанию это поле должно иметь значение NULL или пусто).

Четвертое - всплывающей подсказке для элемента-ссылки.

Пятое - признаку активности для элемента-ссылки.

```xml
<MenuItems>
  <DataConnection SourceDataConnection="SourceDataConnectionName">
    <Fields>
      <Field Name="TitleFieldName" />
      <Field Name="LinkFieldName" />
      <Field Name="ApplicationFieldName" />
      <Field Name="HintFieldName" />
      <Field Name="EnabledFieldName" />
    </Fields>
  </DataConnection>
</MenuItems>
```

### WaitWhileOpen <a href="#wait_while_open" id="wait_while_open"></a>

Признак, определяющий, ожидать ли открытие ссылки в потоке текущей формы или открыть ее в другом потоке.

Необязательный тэг. Ожидается логическое значение.

Если тэг `<WaitWhileOpen>` отсутствует, то используется значение False.

```xml
<WaitWhileOpen>False</WaitWhileOpen>
```

## Get-проперти для получения свойств <a href="#get_properties" id="get_properties"></a>

### ClickedMenuItemValue <a href="#get_clicked_menu_item_value" id="get_clicked_menu_item_value"></a>

Возвращает ссылку, соответствующую последнему выбранному (по которому был совершен клик мышкой) элементу.

```xml
<Object Name="LinkContextMenu">
  <Property Name="ClickedMenuItemValue" />
</Object>
```

### ClickedMenuItemDisplayValue <a href="#get_clicked_menu_item_display_value" id="get_clicked_menu_item_display_value"></a>

Возвращает текст последнего выбранного (по которому был совершен клик мышкой) элемента.

```xml
<Object Name="LinkContextMenu">
  <Property Name="ClickedMenuItemDisplayValue" />
</Object>
```
