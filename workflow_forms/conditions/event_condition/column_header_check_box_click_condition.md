---
description: Событийное условие; срабатывает при клике на CheckBox в заголовке таблицы.
---

# ColumnHeaderCheckBoxClickCondition

## Шаблон ColumnHeaderCheckBoxClickCondition <a href="#template_column_header_check_box_click_condition" id="template_column_header_check_box_click_condition"></a>

```xml
<Condition Name="" Type="ColumnHeaderCheckBoxClickCondition" Assembly="Conditions">
  <Table Name="" />
  <Column Name="" />
</Condition>
```

## Описание ColumnHeaderCheckBoxClickCondition <a href="#description_column_header_check_box_click_condition" id="description_column_header_check_box_click_condition"></a>

```xml
<Condition Name="ColumnHeaderCheckBoxClickCondition" Type="ColumnHeaderCheckBoxClickCondition" Assembly="Conditions">
  <!--Тэги, общие для всех условий-->
  <!--Тэги, специфичные для ColumnHeaderCheckBoxClickCondition-->
</Condition>
```

## Тэги, специфичные для ColumnHeaderCheckBoxClickCondition <a href="#tags_column_header_check_box_click_condition" id="tags_column_header_check_box_click_condition"></a>

### Table <a href="#table" id="table"></a>

[Таблица](../../objects/databasetable/), в которой срабатывает событие клика на `CheckBox` в заголовке.

Обязательный тэг. Значение тэга `<Table>`: не ожидается.

```xml
<Table Name="TableName" />
```

#### Атрибуты тэга `<Table>` <a href="#attributes_tag_table" id="attributes_tag_table"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="463.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название объекта таблицы.</p><p></p><p>Обязательный атрибут. Ожидается название одного из объектов таблиц, описанных в форме.</p></td></tr></tbody></table>

### Column <a href="#column" id="column"></a>

Столбец, в котором срабатывает событие клика на `CheckBox` в заголовке.

Обязательный тэг. Значение тэга `<Column>`: не ожидается.

```xml
<Table Name="ColumnName" />
```

#### Атрибуты тэга `<Column>` <a href="#attributes_tag_column" id="attributes_tag_column"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="463.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название столбца таблицы.</p><p></p><p>Обязательный атрибут. Ожидается название одного из столбцов таблицы.</p></td></tr></tbody></table>
