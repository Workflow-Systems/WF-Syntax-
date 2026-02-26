---
description: >-
  Сохраняющее соединение с данными для объекта дерева базы данных; отправляет
  данные изменения дерева на сервер.
---

# DatabaseTreeSetDataConnection

## Шаблон DatabaseTreeSetDataConnection <a href="#template_database_tree_set_dc" id="template_database_tree_set_dc"></a>

```xml
<DataConnection Name="" Type="DatabaseTreeSetDataConnection" Assembly="ComplexDataConnections">
  <Workflow Name="" />
  <Tree Name="" />
  <NativeNames ItemId="" ItemTitle="" ParentItemId="" />
  <SqlQueries>
    <SqlQuery Name="" Type="Insert" />
    <SqlQuery Name="" Type="Update" />
    <SqlQuery Name="" Type="Transfer" />
    <SqlQuery Name="" Type="Delete" />
  </SqlQueries>
  <Refresh>
    <DataConnection Name="" />
  </Refresh>
</DataConnection>
```

## Описание DatabaseTreeSetDataConnection <a href="#description_database_tree_set_dc" id="description_database_tree_set_dc"></a>

```xml
<DataConnection Name="DatabaseTreeSetDataConnectionName" Type="DatabaseTreeSetDataConnection" Assembly="DataConnections">
  <!--Тэги, специфичные для DatabaseTreeSetDataConnection-->
</DataConnection>
```

## Тэги, специфичные для DatabaseTreeSetDataConnection <a href="#tags_database_tree_set_dc" id="tags_database_tree_set_dc"></a>

### Workflow <a href="#workflow" id="workflow"></a>

Процесс, в рамках которого происходят запросы.

Обязательный тэг. Значение тэга `<Workflow>`: не ожидается.

```xml
<Workflow Name="WorkflowName" />
```

#### Атрибуты тэга `<Workflow>` <a href="#attributes_tag_workflow" id="attributes_tag_workflow"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="466.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название процесса.</p><p></p><p>Обязательный атрибут. Ожидается название одного из процессов, расположенных на сервере и заголовочно описанных в базе.</p></td></tr></tbody></table>

### Tree <a href="#tree" id="tree"></a>

[Объект](../objects/database_tree.md) дерева базы данных, для которого происходит сохранение изменений.

Обязательный тэг. Значение тэга `<Tree>`: не ожидается.

```xml
<Tree Name="TreeName" />
```

#### Атрибуты тэга `<Tree>` <a href="#attributes_tag_tree" id="attributes_tag_tree"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="466.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название объекта дерева базы данных.</p><p></p><p>Обязательный атрибут. Ожидается название одного из объектов дерева базы данных, описанных в форме.</p></td></tr></tbody></table>

### NativeNames <a href="#native_names" id="native_names"></a>

Параметры, передаваемые в запросы.

Обязательный тэг. Значение тэга `<NativeNames>`: не ожидается.

```xml
<NativeNames ItemId="ItemIdName" ItemTitle="ItemTitleName" ParentItemId="ParentItemIdName" />
```

#### Атрибуты тэга `<NativeNames>` <a href="#attributes_tag_native_names" id="attributes_tag_native_names"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="466.3333333333333"></th></tr></thead><tbody><tr><td align="center">ItemId</td><td><p>Название параметра, которое используется в описании запроса на сервере, обозначающего идентификатор элемента.</p><p></p><p>Обязательный атрибут. Ожидается название одного из параметров, использующихся в описании запроса на сервере.</p></td></tr><tr><td align="center">ItemTitle</td><td><p>Название параметра, которое используется в описании запроса на сервере, обозначающего название элемента.</p><p></p><p>Обязательный атрибут. Ожидается название одного из параметров, использующихся в описании запроса на сервере.</p></td></tr><tr><td align="center">ParentItemIdName</td><td><p>Название параметра, которое используется в описании запроса на сервере, обозначающего идентификатор родительского элемента.</p><p></p><p>Обязательный атрибут. Ожидается название одного из параметров, использующихся в описании запроса на сервере.</p></td></tr></tbody></table>

### SqlQueries <a href="#sql_queries" id="sql_queries"></a>

Запросы для отправки данных.

Обязательный тэг. Значение тэга `<SqlQueries>`: список тэгов [`<SqlQuery>`](database_tree_set_dc.md#sql_queries_sql_query).

В insert-запросы передаются параметры новых узлов дерева, в update-запросы - измененных узлов, в delete-запросы - удаленных узлов, в transfer-запросы - перенесенных узлов.

```xml
<SqlQueries>
  <SqlQuery Name="InsertSqlQuery" Type="Insert" />
  <SqlQuery Name="UpdateSqlQuery" Type="Update" />
  <SqlQuery Name="DeleteSqlQuery" Type="Delete" />
  <SqlQuery Name="TransferSqlQuery" Type="Transfer" />
</SqlQueries>
```

#### Тэг `<SqlQuery>` <a href="#sql_queries_sql_query" id="sql_queries_sql_query"></a>

Запрос для отправки данных.

Обязательный тэг. Значение тэга `<SqlQuery>`: не ожидается.

#### Атрибуты тэга `<SqlQuery>` <a href="#attributes_tag_sql_queries_sql_query" id="attributes_tag_sql_queries_sql_query"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="466.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название запроса.</p><p></p><p>Обязательный атрибут. Ожидается название одного из запросов, описанных на сервере.</p></td></tr><tr><td align="center">Type</td><td><p>Тип запроса.</p><p></p><p>Обязательный атрибут. Ожидается значение Insert, Update, Delete или Transfer.</p></td></tr></tbody></table>

### Refresh <a href="#refresh" id="refresh"></a>

Загружающие соединения с данными, которые будет обновлены после выполнения сохранения.

Обязательный тэг. Значение тэга `<Refresh>`: список тэгов [`<DataConnection>`](database_tree_set_dc.md#refresh_data_connection).

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
