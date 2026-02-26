---
description: Обычное контекстное меню.
---

# ContextMenu

## Шаблон ContextMenu <a href="#template" id="template"></a>

```xml
<ContextMenu Name="">
  <MenuItem />
  <MenuItem />
</ContextMenu>
```

## Описание ContextMenu <a href="#description" id="description"></a>

```xml
<ContextMenu Name="ContextMenuName">
  <!--Тэги, общие для всех контекстных меню-->
  <!--Тэги, специфичные для ContextMenu-->
</ContextMenu>
```

## Тэги, специфичные для ContextMenu <a href="#specific-tags" id="specific-tags"></a>

### MenuItem <a href="#menu_item" id="menu_item"></a>

[Элементы меню](../menu_item/).

Необязательный список тэгов.

```xml
<MenuItem />
<MenuItem />
```

## Get-проперти для получения свойств <a href="#get_properties" id="get_properties"></a>

### ClickedMenuItemDisplayValue <a href="#get_clicked_menu_item_display_value" id="get_clicked_menu_item_display_value"></a>

Возвращает текст последнего выбранного (по которому был совершен клик мышкой) элемента.

```xml
<Object Name="ContextMenu">
  <Property Name="ClickedMenuItemDisplayValue" />
</Object>
```
