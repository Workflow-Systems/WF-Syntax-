---
description: Запрос для получения данных с сервера.
---

# SqlQuery

## Шаблон SqlQuery <a href="#template_primary_dc" id="template_primary_dc"></a>

```xml
<SqlQuery Name="" Type="Select">
  <ManualLoad></ManualLoad> 
  <Workflow Name="" />
  <Fields>
    <Field Name="" NativeName="" />
    <Field Name="" Type="FormatField" FormatString="">
      <Field NativeName="" />
      <Field NativeName="" />
    </Field>
  </Fields>
  <Parameters>
    <Parameter NativeName="" RefreshQuery="" SendAsArray="">
      <Value></Value>
      <IfNull></IfNull>
      <IfEmpty></IfEmpty>
    </Parameter>
  </Parameters>
  <Filter>
    <And RefreshFilter="">
      <Or RefreshFilter="">
        <Filter Type="" FilterByNullValue="" RefreshFilter="" Reverse="">
          <Field NativeName="" />
          <Value></Value>
          <DataType Type="" />
          <Enabled></Enabled>
        </Filter>
        <Filter Type="" FilterByNullValue="" RefreshFilter="" Reverse="">
          <Field NativeName="" />
          <Value></Value>
          <DataType Type="" />
          <Enabled></Enabled>
        </Filter>
      </Or>
      <Not RefreshFilter="">
        <Filter Type="" FilterByNullValue="" RefreshFilter="" Reverse="">
          <Field NativeName="" />
          <Value></Value>
          <DataType Type="" />
          <Enabled></Enabled>
        </Filter>
      </Not>
    </And>
  </Filter>
</SqlQuery>
```

## Описание SqlQuery <a href="#description_primary_dc" id="description_primary_dc"></a>

```xml
<SqlQuery Name="">
  <ManualLoad></ManualLoad> 
  <Workflow Name="" />
  <Fields></Fields>
  <Parameters></Parameters>
  <Filter></Filter>
</SqlQuery>
```

## Тэги, специфичные для SqlQuery <a href="#option_1_tags_primary_dc" id="option_1_tags_primary_dc"></a>

### ManualLoad <a href="#sql_query_manual_load" id="sql_query_manual_load"></a>

Признак, определяющий, будет ли загрузка данных происходить только после ручного обновления соединения с данными, а не вместе с загрузкой формы.

```xml
<ManualLoad>False</ManualLoad>
```

Необязательный тэг. Ожидается логическое значение.

Если тэг `<ManualLoad>` отсутствует, то наследуется значение тэга [`<ManualLoad>`](sql_query.md#manual_load) соединения с данными.

### Workflow <a href="#sql_query_workflow" id="sql_query_workflow"></a>

Процесс, в рамках которого происходит запрос.

```xml
<Workflow Name="WorkflowName" />
```

Обязательный тэг. Значение тэга не ожидается.

В качестве значения атрибута `Name` ожидается название одного из процессов, расположенных на сервере и заголовочно описанных в базе данных в таблице public.workflow\_type.

### Fields <a href="#sql_query_fields" id="sql_query_fields"></a>

Список полей запроса.

```xml
<Fields>
  <Field Name="field_name1" />
  <Field Name="FieldName2" NativeName="field_name2" />
  <Field Name="FieldName3" Type="FormatField" FormatString="{0} ({1})">
    <Field NativeName="field_name3" />
    <Field NativeName="field_name4" />
  </Field>
</Fields>
```

Обязательный тэг. Ожидается список тегов `<Field>`.

Обязательный атрибут `Name` - название поля запроса, которое будет использоваться на форме. Если атрибут `NativeName` присутствует, то в качестве значения атрибута `Name` ожидается любое значение. Если атрибут `NativeName` отсутствует, то ожидается название одного из полей, возвращаемых запросом.

Необязательный атрибут `NativeName` - название поля запроса, описанного на сервере. Ожидается название одного из полей, возвращаемых запросом.

{% hint style="info" %}
Суть связи атрибутов `Name` и `NativeName` - переименование полей запроса.
{% endhint %}

Необязательный атрибут `Type` - тип поля. Ожидается тип FormatField.

Необязательный атрибут `FormatString` задает формат строки для объединения значений нескольких полей. Значение атрибута любая строка, поддерживающая выражения вида "{n}", где n - индекс вложенного поля, начинающийся с 0.

### Parameters <a href="#sql_query_parameters" id="sql_query_parameters"></a>

Список параметров, передаваемых в запрос.

```xml
<Parameters>
  <Parameter NativeName="NativeName" RefreshQuery="False" SendAsArray="True">
    <Value>Value</Value>
    <IfNull>Value</IfNull>
    <IfEmpty>Value</IfEmpty>
  </Parameter>
</Parameters>
```

Необязательный тэг. Ожидается список тэгов `<Parameter>`.

### Parameter <a href="#tags_sql_query_parameters_parameter" id="tags_sql_query_parameters_parameter"></a>

```xml
<Parameter NativeName="NativeName" RefreshQuery="False" SendAsArray="True">
  <Value>Value</Value>
  <IfNull>Value</IfNull>
  <IfEmpty>Value</IfEmpty>
</Parameter>
```

Обязательный атрибут `NativeName` - название параметра, которое используется в SQL-запросе. Ожидается название одного из параметров, использующихся в SQL-запросе на сервере.

Необязательный атрибут `RefreshQuery` - признак, определяющий, будут ли обновлены данные запроса при изменении значения параметра. Ожидается логическое значение.\
Если атрибут `RefreshQuery` отсутствует, то используется значение True.

{% hint style="info" %}
Применять значение False для атрибута `RefreshQuery` имеет смысл тогда, когда обновляется более одного параметра запроса одновременно, но при этом нет необходимости выполнять запросы отдельно при обновлении каждого параметра.
{% endhint %}

Необязательный атрибут `SendAsArray` - признак, определяющий будет ли значение передаваться как массив. Ожидается логическое значение.\
Если атрибут `SendAsArray` отсутствует, то используется значение False.

#### Вложенные тэги тэга `<Parameter>` <a href="#tags_sql_query_parameters_parameter" id="tags_sql_query_parameters_parameter"></a>

Обязательный тэг `<Value>` - значение параметра.\
Ожидается любое значение.

Необязательный тэг `<IfNull>` - значение, которое будет передано в качестве значение параметра, если последний в тэге `<Value>` имеет значение NULL.\
Ожидается любое значение.

Необязательный тэг `<IfEmpty>` - значение, которое будет передано в качестве значение параметра, если последний в тэге `<Value>` имеет значение "".\
Ожидается любое значение.

### Filter <a href="#sql_query_filter" id="sql_query_filter"></a>

Фильтр полученных данных.

{% hint style="info" %}
Фильтрация происходит без повторных запросов в базу данных.
{% endhint %}

Необязательный тэг.

Может быть двух видов: одиночный фильтр и составной. Подробное описание тэга `<Filter>` доступно по [ссылке](filter.md).

Вариант одиночного фильтра:

```xml
<Filter Type="Equal" FilterByNullValue="True" RefreshFilter="True" Reverse="True">
  <Field NativeName="" />
  <Value></Value>
  <DataType Type="" />
  <Enabled></Enabled>
</Filter>
```

Вариант составного фильтра:

```xml
<Filter Type="" FilterByNullValue="">
  <And RefreshFilter="" RefreshData="">
    <Or RefreshFilter="" RefreshData="">
      <Filter Type="" FilterByNullValue="" RefreshFilter="" Reverse="">
        <Field NativeName="" />
        <Value></Value>
        <DataType Type="" />
        <Enabled></Enabled>
      </Filter>
      <Filter Type="" FilterByNullValue="" RefreshFilter="" Reverse="">
        <Field NativeName="" />
        <Value></Value>
        <Enabled></Enabled>
      </Filter>
    </Or>
    <Not RefreshFilter="" RefreshData="">
      <Filter Type="" FilterByNullValue="" RefreshFilter="" Reverse="">
        <Field NativeName="" />
        <Value></Value>
        <DataType Type="" />
        <Enabled></Enabled>
      </Filter>
    </Not>
  </And>
</Filter>
```

