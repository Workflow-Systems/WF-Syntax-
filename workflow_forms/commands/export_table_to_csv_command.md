---
description: Команда; экспортирует данные из таблицы в файл формата CSV.
---

# ExportTableToCsvCommand

## Шаблон ExportTableToCsvCommand <a href="#template_export_table_to_csv_command" id="template_export_table_to_csv_command"></a>

```xml
<Command Name="" Type="ExportTableToCsvCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для ExportTableToCsvCommand-->
  <Async Value="" />
  <Table Name="TableName" />
  <ExcludeColumnHeaders Value="" />
  <Columns>
    <Column Name=""></Column>
    <Column Name=""></Column>
  </Columns>
  <FilterRows ColumnName=""></FilterRows>
  <ExportPath Ask=""></ExportPath>
  <Open></Open>
</Command>
```

## Описание ExportTableToCsvCommand <a href="#description_export_table_to_csv_command" id="description_export_table_to_csv_command"></a>

```xml
<Command Name="ExportTableToCsvCommandName" Type="ExportTableToCsvCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для ExportTableToCsvCommand-->
</Command>
```

### Результат выполнения ExportTableToCsvCommand <a href="#result_export_table_to_csv_command" id="result_export_table_to_csv_command"></a>

#### Value <a href="#result_value" id="result_value"></a>

Полный путь с названием файла, в который было выгружено содержимое.

## Тэги, специфичные для ExportTableToCsvCommand <a href="#tags_export_table_to_csv_command" id="tags_export_table_to_csv_command"></a>

### Async <a href="#async" id="async"></a>

Признак, определяющий, будет ли выполнение команды происходить в асинхронном режиме (в фоновом потоке).

Необязательный тэг. Значение тэга `<Async>`: не ожидается.

Если тэг `<Async>` отсутствует, то для атрибута `Value` используется значение False.

```xml
<Async Value="False" />
```

#### Атрибуты тэга `<Async>` <a href="#attributes_tag_async" id="attributes_tag_async"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

### Table <a href="#table" id="table"></a>

Таблица, данные которой будут выгружаться в файл.

Обязательный тэг. Значение тэга `<Table>`: не ожидается.

```xml
<Table Name="TableName" />
```

#### Атрибуты тэга `<Table>` <a href="#attributes_tag_table" id="attributes_tag_table"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название одной из таблиц, описанных в форме.</p><p></p><p>Обязательный атрибут. Ожидается название одной из таблиц, описанных в форме.</p></td></tr></tbody></table>

### ExcludeColumnHeaders <a href="#exclude_column_headers" id="exclude_column_headers"></a>

Признак, определяющий, экспортировать ли заголовки столбцов.

Необязательный тэг. Значение тэга `<ExcludeColumnHeaders>`: не ожидается.

Если тэг `<ExcludeColumnHeaders>` отсутствует, то для атрибута `Value` используется значение False.

```xml
<ExcludeColumnHeaders Value="False" />
```

#### Атрибуты тэга `<ExcludeColumnHeaders>` <a href="#attributes_tag_exclude_column_headers" id="attributes_tag_exclude_column_headers"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

### Columns <a href="#columns" id="columns"></a>

Экспортируемые столбцы.

Необязательный тэг. Значение тэга `<Columns>`: список тэгов [`<Column>`](export_table_to_csv_command.md#columns_column).

Если тэг `<Columns>` отсутствует, то экспортируются все видимые столбцы таблицы.

```xml
<Columns>
  <Column Name="ColumnName1">True</Column>
  <Column Name="ColumnName2">False</Column>
  <Column Name="ColumnName3" />
</Columns>
```

#### Тэг `<Column>` <a href="#columns_column" id="columns_column"></a>

Экспортируемый столбец с признаком, задаваемым в значении тэга `<Column>`, следует ли его экспортировать.

Необязательный тэг. Ожидается логическое значение.

Если значение тэга `<Column>` равно NULL, то столбец считается экспортируемым.

#### Атрибуты тэга `<Column>` <a href="#attributes_tag_columns_column" id="attributes_tag_columns_column"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Имя столбца.</p><p></p><p>Обязательный атрибут. Значение атрибута <code>Name</code>: имя одного из столбцов указанной таблицы.</p></td></tr></tbody></table>

### FilterRows <a href="#filter_rows" id="filter_rows"></a>

Фильтрация экспортируемых строк по соответствию значений определенного столбца набору определенных значений.

Необязательный тэг. Ожидается любое скалярное значение или линейный масси&#x432;**.**

Если тэг `<FilterRows>` отсутствует, то экспортируются все видимые строки таблицы.

```xml
<FilterRows ColumnName=""></FilterRows>
```

#### Атрибуты тэга `<FilterRows>` <a href="#attributes_tag_filter_rows" id="attributes_tag_filter_rows"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">ColumnName</td><td><p>Имя столбца, значения которого будут сравниваться с набором значений из тэга <code>&#x3C;FilterRows></code>.</p><p></p><p>Обязательный атрибут. Значение атрибута <code>ColumnName</code>: имя одного из столбцов указанной таблицы.</p></td></tr></tbody></table>

### ExportPath <a href="#export_path" id="export_path"></a>

Путь до папки, в которой будет расположен файл с выгруженными данными.

Необязательный тэг. Любое значение будет переведено в текстовое.

Если тэг `<ExportPath>` отсутствует, то используется пустое значение, а для атрибута `Ask` используется значение False.

Поддерживаются [константы замены](../values/replacement_constants.md).

```xml
<ExportPath Ask="False">ExportPath</ExportPath>
```

#### Атрибуты тэга `<ExportPath>` <a href="#attributes_tag_export_path" id="attributes_tag_export_path"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Ask</td><td><p>Признак, определяющий, будет ли вызвано диалоговое окно для выбора файла для экспорта.</p><p></p><p>Необязательный атрибут. Ожидается логическое значение.</p><p></p><p>Если атрибут <code>Ask</code> отсутствует, то используется значение False.</p></td></tr></tbody></table>

### Open <a href="#open" id="open"></a>

Признак открытия CSV-файла после формирования.

Необязательный тэг. Ожидается логическое значение.

Если тэг `<Open>` отсутствует, то используется значение False.

```xml
<Open>False</Open>
```
