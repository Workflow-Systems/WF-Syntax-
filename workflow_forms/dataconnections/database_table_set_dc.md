---
description: >-
  Сохраняющее соединение с данными для объекта таблицы базы данных; отправляет
  данные изменения таблицы на сервер.
---

# DatabaseTableSetDataConnection

## Шаблон DatabaseTableSetDataConnection <a href="#template_database_table_set_dc" id="template_database_table_set_dc"></a>

```xml
<DataConnection Name="" Type="DatabaseTableSetDataConnection" Assembly="ComplexDataConnections">
  <Workflow Name="" />
  <DatabaseTable Name="" />
  <AutoSave Value="" />
  <Parameters>
    <Parameter NativeName="">
      <Column Name="" />
    </Parameter>
    <Parameter NativeName=""></Parameter>
  </Parameters>
  <SqlQueries>
    <SqlQuery Name="" Type="Insert" />
    <SqlQuery Name="" Type="Update" />
    <SqlQuery Name="" Type="Delete" />
  </SqlQueries>
  <Refresh>
    <DataConnection Name="" />
  </Refresh>
</DataConnection>
```

## Описание DatabaseTableSetDataConnection <a href="#description_database_table_set_dc" id="description_database_table_set_dc"></a>

```xml
<DataConnection Name="DatabaseTableSetDataConnectionName" Type="DatabaseTableSetDataConnection" Assembly="DataConnections">
  <!--Тэги, общие для всех соединений с данными-->
  <!--Тэги, специфичные для DatabaseTableSetDataConnection-->
</DataConnection>
```

## Тэги, специфичные для DatabaseTableSetDataConnection <a href="#tags_database_table_set_dc" id="tags_database_table_set_dc"></a>

### Workflow <a href="#workflow" id="workflow"></a>

Процесс, в рамках которого происходят запросы.

Обязательный тэг. Значение тэга `<Workflow>`: не ожидается.

```xml
<Workflow Name="WorkflowName" />
```

#### Атрибуты тэга `<Workflow>` <a href="#attributes_tag_workflow" id="attributes_tag_workflow"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="471.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название процесса.</p><p></p><p>Обязательный атрибут. Ожидается название одного из процессов, расположенных на сервере и заголовочно описанных в базе.</p></td></tr></tbody></table>

### DatabaseTable <a href="#database_table" id="database_table"></a>

Объект [таблицы](../objects/databasetable/) базы данных, для которой происходит сохранение изменений.

Обязательный тэг. Значение тэга `<DatabaseTable>`: не ожидается.

```xml
<DatabaseTable Name="DatabaseTableName" />
```

#### Атрибуты тэга `<DatabaseTable>` <a href="#attributes_tag_database_table" id="attributes_tag_database_table"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="471.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название объекта таблицы базы данных.</p><p></p><p>Обязательный атрибут. Ожидается название одного из объектов таблицы базы данных, описанных в форме.</p></td></tr></tbody></table>

### AutoSave <a href="#auto_save" id="auto_save"></a>

Признак, определяющий, будет ли соединение сохранять таблицу в базу данных.

Необязательный тэг. Значение тэга `<AutoSave>`: не ожидается.

Если тэг `<AutoSave>` не задан, то для атрибута `Value` используется значение False.

```xml
<AutoSave Value="False" />
```

#### Атрибуты тэга `<AutoSave>` <a href="#attributes_tag_auto_save" id="attributes_tag_auto_save"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="471.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

### Parameters <a href="#parameters" id="parameters"></a>

Параметры, передаваемые в запросы.

Необязательный тэг. Значение тэга `<Parameters>`: список тэгов [`<Parameter>`](database_table_set_dc.md#parameters_parameter).

```xml
<Parameters>
  <Parameter NativeName="NativeName">
    <Column Name="ColumnName" />
  </Parameter>
</Parameters>
```

#### Тэг `<Parameter>` <a href="#parameters_parameter" id="parameters_parameter"></a>

Параметр, передаваемый в запросы.

Необязательный тэг. Ожидается любое значение, либо тэг [`<Column>`](database_table_set_dc.md#parameters_parameter_column).

#### Тэг `<Column>` <a href="#parameters_parameter_column" id="parameters_parameter_column"></a>

Колонка, из которой будут подставляться значения в качестве соответствующего параметра.

Необязательный тэг. Значение тэга `<Column>`: не ожидается.

#### Атрибуты тэга `<Column>` <a href="#attributes_tag_parameters_parameter_column" id="attributes_tag_parameters_parameter_column"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="471.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название колонки объекта таблицы базы данных.</p><p></p><p>Обязательный атрибут. Ожидается название одной из колонок объекта таблицы базы данных.</p></td></tr></tbody></table>

### SqlQueries <a href="#sql_queries" id="sql_queries"></a>

Запросы для отправки данных.

Обязательный тэг. Значение тэга `<SqlQueries>`: список тэгов [`<SqlQuery>`](database_table_set_dc.md#sql_queries_sql_query).

В insert-запросы передаются параметры новых строк таблицы, в update-запросы - измененных строк, в delete-запросы - удаленных строк.

```xml
<SqlQueries>
  <SqlQuery Name="InsertSqlQuery" Type="Insert" />
  <SqlQuery Name="UpdateSqlQuery" Type="Update" />
  <SqlQuery Name="DeleteSqlQuery" Type="Delete" />
</SqlQueries>
```

#### Тэг `<SqlQuery>` <a href="#sql_queries_sql_query" id="sql_queries_sql_query"></a>

Запрос для отправки данных.

Обязательный тэг. Значение тэга `<SqlQuery>`: не ожидается.

#### Атрибуты тэга `<SqlQuery>` <a href="#attributes_tag_sql_queries_sql_query" id="attributes_tag_sql_queries_sql_query"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="471.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название запроса.</p><p></p><p>Обязательный атрибут. Ожидается название одного из запросов, описанных на сервере.</p></td></tr><tr><td align="center">Type</td><td><p>Тип запроса.</p><p></p><p>Обязательный атрибут. Ожидается значение Insert, Update или Delete.</p></td></tr></tbody></table>

### Refresh <a href="#refresh" id="refresh"></a>

Загружающие [соединения с данными](./), которые будет обновлены после выполнения сохранения.

Обязательный тэг. Значение тэга `<Refresh>`: список тэгов [`<DataConnection>`](database_table_set_dc.md#refresh_data_connection).

```xml
<Refresh>
  <DataConnection Name="DataConnectionName1" />
  <DataConnection Name="DataConnectionName2" />
</Refresh>
```

#### Тэг `<DataConnection>` <a href="#refresh_data_connection" id="refresh_data_connection"></a>

Загружающие соединение с данными, которое будет обновлено.

Необязательный тэг.

#### Атрибуты тэга `<DataConnection>` <a href="#attributes_tag_refresh_data_connection" id="attributes_tag_refresh_data_connection"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="471.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название загружающего соединения с данными.</p><p></p><p>Обязательный атрибут. Ожидается название одного из загружающих соединений с данными, описанных в форме.</p></td></tr></tbody></table>
