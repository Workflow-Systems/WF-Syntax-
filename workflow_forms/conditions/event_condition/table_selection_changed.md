---
description: Событийное условие; срабатывает при изменении выделения в таблице.
---

# TableSelectionChanged

## Шаблон TableSelectionChanged <a href="#template_table_selection_changed" id="template_table_selection_changed"></a>

```xml
<Condition Name="" Type="TableSelectionChanged" Assembly="Conditions">
  <!--Тэги, общие для всех условий-->
  <AlwaysChange Value="" />
  <!--Тэги, специфичные для TableSelectionChanged-->
  <Table Name="" />
</Condition>
```

## Описание TableSelectionChanged <a href="#description_table_selection_changed" id="description_table_selection_changed"></a>

```xml
<Condition Name="TableSelectionChangedName" Type="TableSelectionChanged" Assembly="Conditions">
  <!--Тэги, общие для всех условий-->
  <!--Тэги, специфичные для TableSelectionChanged-->
</Condition>
```

## Тэги, специфичные для TableSelectionChanged <a href="#tags_table_selection_changed" id="tags_table_selection_changed"></a>

### Table <a href="#table" id="table"></a>

Таблица, в которой срабатывает событие изменения выделения.

Обязательный тэг. Значение тэга `<Table>`: не ожидается.

```xml
<Table Name="TableName" />
```

#### Атрибуты тэга `<Table>` <a href="#attributes_tag_table" id="attributes_tag_table"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="465.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название объекта <a href="../../objects/databasetable/">таблицы</a>.</p><p></p><p>Обязательный атрибут. Ожидается название одного из объектов таблиц, описанных в форме.</p></td></tr></tbody></table>
