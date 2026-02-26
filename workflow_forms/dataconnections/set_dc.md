---
description: Сохраняющее соединение с данными; отправляет данные на сервер.
---

# SetDataConnection

## Шаблон SetDataConnection <a href="#template_set_dc" id="template_set_dc"></a>

```xml
<DataConnection Name="" Type="SetDataConnection" Assembly="DataConnections">
  <Workflow Name="" />
  <Parameters>
    <Parameter NativeName="" SendAsArray="">
      <Value></Value>
      <IfNull></IfNull>
      <IfEmpty></IfEmpty>
    </Parameter>
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

## Описание SetDataConnection <a href="#description_set_dc" id="description_set_dc"></a>

```xml
<DataConnection Name="SetDataConnectionName" Type="SetDataConnection" Assembly="DataConnections">
  <!--Тэги, специфичные для SetDataConnection-->
</DataConnection>
```

## Тэги, специфичные для SetDataConnection <a href="#tags_set_dc" id="tags_set_dc"></a>

### Workflow <a href="#workflow" id="workflow"></a>

Процесс, в рамках которого происходят запросы.

Обязательный тэг. Значение тэга `<Workflow>`: не ожидается.

```xml
<Workflow Name="WorkflowName" />
```

#### Атрибуты тэга `<Workflow>` <a href="#attributes_tag_workflow" id="attributes_tag_workflow"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="466.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название процесса.</p><p></p><p>Обязательный атрибут. Ожидается название одного из процессов, расположенных на сервере и заголовочно описанных в базе.</p></td></tr></tbody></table>

### Parameters <a href="#parameters" id="parameters"></a>

Параметры, передаваемые в запросы.

Необязательный тэг. Значение тэга `<Parameters>`: список тэгов [`<Parameter>`](set_dc.md#parameters_parameter).

```xml
<Parameters>
  <Parameter NativeName="NativeName" SendAsArray="True">
    <Value>Value</Value>
    <IfNull>Value</IfNull>
    <IfEmpty>Value</IfEmpty>
  </Parameter>
</Parameters>
```

#### Тэг `<Parameter>` <a href="#parameters_parameter" id="parameters_parameter"></a>

Параметр, передаваемый в запросы.

Необязательный тэг. Значение тэга `<Parameter>`: список тэгов [`<Value>`](set_dc.md#parameters_parameter_value), [`<IfNull>`](set_dc.md#parameters_parameter_if_null) и [`<IfEmpty>`](set_dc.md#parameters_parameter_if_empty).

#### Атрибуты тэга `<Parameter>` <a href="#attributes_tag_parameters_parameter" id="attributes_tag_parameters_parameter"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="466.3333333333333"></th></tr></thead><tbody><tr><td align="center">NativeName</td><td><p>Название параметра, которое используется в описании запроса на сервере.</p><p></p><p>Обязательный атрибут. Ожидается название одного из параметров, использующихся в описании запроса на сервере.</p></td></tr><tr><td align="center">SendAsArray</td><td><p>Признак, определяющий будет ли значение передаваться как массив.</p><p></p><p>Необязательный атрибут. Ожидается логическое значение.</p><p></p><p>Если атрибут <code>SendAsArray</code> отсутствует, то используется значение False.</p></td></tr></tbody></table>

#### Тэг `<Value>` <a href="#parameters_parameter_value" id="parameters_parameter_value"></a>

Значение параметра.

Обязательный тэг. Ожидается любое значение.

#### Тэг `<IfNull>` <a href="#parameters_parameter_if_null" id="parameters_parameter_if_null"></a>

Значение, которое будет передано в качестве значение параметра, если последний в тэге [`<Value>`](set_dc.md#parameters_parameter_value) имеет значение NULL.

Обязательный тэг. Ожидается любое значение.

#### Тэг `<IfEmpty>` <a href="#parameters_parameter_if_empty" id="parameters_parameter_if_empty"></a>

Значение, которое будет передано в качестве значение параметра, если последний в тэге [`<Value>`](set_dc.md#parameters_parameter_value) имеет значение "".

Обязательный тэг. Ожидается любое значение.

### SqlQueries <a href="#sql_queries" id="sql_queries"></a>

Запросы для отправки данных.

Обязательный тэг. Значение тэга `<SqlQueries>`: список тэгов [`<SqlQuery>`](set_dc.md#sql_queries_sql_query).

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

<table data-header-hidden><thead><tr><th align="center"></th><th width="466.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название запроса.</p><p></p><p>Обязательный атрибут. Ожидается название одного из запросов, описанных на сервере.</p></td></tr><tr><td align="center">Type</td><td><p>Тип запроса.</p><p></p><p>Обязательный атрибут. Ожидается значение Insert, Update или Delete.</p></td></tr></tbody></table>

### Refresh <a href="#refresh" id="refresh"></a>

Загружающие соединения с данными, которые будет обновлены после выполнения сохранения.

Необязательный тэг. Значение тэга `<Refresh>`: список тэгов [`<DataConnection>`](set_dc.md#refresh_data_connection).

```xml
<Refresh>
  <DataConnection Name="DataConnectionName1" />
  <DataConnection Name="DataConnectionName2" />
</Refresh>
```

#### Тэг `<DataConnection>` <a href="#refresh_data_connection" id="refresh_data_connection"></a>

Загружающее соединение с данными, которое будет обновлено.

Необязательный тэг.&#x20;

#### Атрибуты тэга `<DataConnection>` <a href="#attributes_tag_refresh_data_connection" id="attributes_tag_refresh_data_connection"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="466.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название загружающего соединения с данными.</p><p></p><p>Обязательный атрибут. Ожидается название одного из загружающих соединений с данными, описанных в форме.</p></td></tr></tbody></table>
