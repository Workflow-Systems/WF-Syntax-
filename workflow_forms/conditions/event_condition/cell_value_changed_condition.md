---
description: >-
  Событийное условие; срабатывает при изменении значения в определенных строках
  и/или столбцах таблицы.
---

# CellValueChangedCondition

## Шаблон CellValueChangedCondition <a href="#template_cell_value_changed_condition" id="template_cell_value_changed_condition"></a>

```xml
<Condition Name="" Type="CellValueChangedCondition" Assembly="Conditions">
  <!--Тэги, общие для всех условий-->
  <AlwaysChange Value="" />
  <!--Тэги, специфичные для CellValueChangedCondition-->
  <Table Name="" />
  <RowIndex></RowIndex>
  <ColumnName></ColumnName>
</Condition>
```

## Описание CellValueChangedCondition <a href="#description_cell_value_changed_condition" id="description_cell_value_changed_condition"></a>

```xml
<Condition Name="CellValueChangedConditionName" Type="CellValueChangedCondition" Assembly="Conditions">
  <!--Тэги, общие для всех условий-->
  <!--Тэги, специфичные для CellValueChangedCondition-->
</Condition>
```

## Тэги, специфичные для CellValueChangedCondition <a href="#tags_cell_value_changed_condition" id="tags_cell_value_changed_condition"></a>

### Table <a href="#table" id="table"></a>

[Таблица](../../objects/databasetable/), в которой срабатывает событие изменения значения ячейки.

Обязательный тэг. Значение тэга `<Table>`: не ожидается.

```xml
<Table Name="TableName" />
```

#### Атрибуты тэга `<Table>` <a href="#attributes_tag_table" id="attributes_tag_table"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="463.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название объекта таблицы.</p><p></p><p>Обязательный атрибут. Ожидается название одного из объектов таблиц, описанных в форме.</p></td></tr></tbody></table>

### RowIndex <a href="#row_index" id="row_index"></a>

Индексы строк таблицы, в которых будет происходить изменения значений в ячейках.

Необязательный тэг. Любое значение будет переведено в массив целочисленных значений.

Если тэг `<RowIndex>` отсутствует, то отслеживание изменений будет происходить во всех строках таблицы.

```xml
<RowIndex>0</RowIndex>
```

### ColumnName <a href="#column_name" id="column_name"></a>

Названия столбцов таблицы, при изменении значений в ячейках которых условие будет срабатывать.

Необязательный тэг. Любое значение будет переведено в массив текстовых значений.

Если тэг `<ColumnName>` отсутствует, то отслеживание изменений будет происходить во всех столбцах таблицы.

```xml
<ColumnName>0</ColumnName>
```
