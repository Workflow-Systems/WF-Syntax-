---
description: >-
  Преобразующее загружающее соединение с данными; на основе данных из двух
  загружающих соединений с данными строит дерево данных.
---

# TreeGetDataConnection

## Шаблон TreeGetDataConnection <a href="#template_tree_get_dc" id="template_tree_get_dc"></a>

```xml
<DataConnection Name="" Type="TreeGetDataConnection" Assembly="DataConnections">
  <ManualRefresh />
  <SourceDataConnection Name="" Query="">
    <Fields>
      <Field Name="" />
      <Field Name="" />
      <Field Name="" />
    </Fields>
  </SourceDataConnection>
  <RelationshipDataConnection Name="" Query="">
    <Fields>
      <Field Name="" />
      <Field Name="" />
    </Fields>
  </RelationshipDataConnection>
  <AdditionalColumns>
    <HasChildrenColumn Name="" />
    <StateColumn Name="" CloseState="" OpenState="" />
  </AdditionalColumns>
  <Order>
    <By Name="" Type="" />
  </Order>
  <Filter Type="">
    <And>
      <Filter FilterByNullValue="">
        <Field NativeName="" />
        <Value>
          <Object Name="" />
        </Value>
        <DataType Type="" />
      </Filter>
      <Filter Type="" FilterByNullValue="">
        <Field NativeName="" />
        <Value>
          <Object Name="" />
        </Value>
        <DataType Type="" />
      </Filter>
    </And>
  </Filter>
</DataConnection>
```

## Тэги, специфичные для TreeGetDataConnection <a href="#tags_tree_get_dc" id="tags_tree_get_dc"></a>

### SourceDataConnection <a href="#source_data_connection" id="source_data_connection"></a>

Элементы дерева.

```xml
<SourceDataConnection Name="SourceDataConnectionName" Query="SqlQueryName">
  <Fields>
    <Field Name="ItemId" />
    <Field Name="Title" />
    <Field Name="Expand" />
    <!-- Дополнительные поля -->    
    <Field Name="FieldName" />
  </Fields>
</SourceDataConnection>
```

Обязательный тэг. В качестве значения ожидается список с тремя обязательными полями и любым количеством дополнительных полей.

Порядок обязательных полей строго определен:

* первое поле должно соответствовать идентификатору элемента;
* второе - его отображаемому значению;
* третье - его состоянию, свернут или развернут узел дерева, если он имеет дочерние элементы.

Обязательный атрибут `Name` - имя соединения с данными. Ожидается имя одного из соединений с данными, описанных на форме.

Необязательный атрибут `Query` - имя запроса из загружающего соединения с данными, если в качестве источника данных указан [PrimaryGetDataConnection](primary_dc/) с несколькими запросами SqlQuery. Ожидается имя одного из запросов, описанных в загружающем соединении с данными.

{% hint style="info" %}
Если в качестве источника данных используется PrimaryGetDataConnection с несколькими запросами и не указан атрибут `SqlQuery` с именем конкретного запроса, то будет использоваться результат запроса первого в порядке описания в синтаксисе PrimaryGetDataConnection.
{% endhint %}

### RelationshipDataConnection <a href="#relationship_data_connection" id="relationship_data_connection"></a>

Взаимосвязи элементов дерева.

```xml
<RelationshipDataConnection Name="SourceDataConnectionName" Query="SqlQueryName">
  <Fields>
    <Field Name="ChildId" />
    <Field Name="ParentId" />
  </Fields>
</RelationshipDataConnection>
```

Обязательный тэг. В качестве значения ожидается список из двух обязательных полей, где первое поле должно соответствовать идентификатору элемента, а второе - идентификатору родительского элемента.

Обязательный атрибут `Name` - имя соединения с данными. Ожидается имя одного из соединений с данными, описанных на форме.

Необязательный атрибут `Query` - имя запроса из загружающего соединения с данными, если в качестве источника данных указан [PrimaryGetDataConnection](primary_dc/) с несколькими запросами SqlQuery. Ожидается имя одного из запросов, описанных в загружающем соединении с данными.

{% hint style="info" %}
Если в качестве источника данных используется PrimaryGetDataConnection с несколькими запросами и не указан атрибут `SqlQuery` с именем конкретного запроса, то будет использоваться результат запроса первого в порядке описания в синтаксисе PrimaryGetDataConnection.
{% endhint %}

### ManualRefresh <a href="#manual_refresh" id="manual_refresh"></a>

Признак, определяющий условия обновления полученных данных. Если значение True, то обновление будет происходить только в ручном режиме при выполнении команды [DataConnectionRefreshCommand](../commands/dc_refresh_command.md). Если значение False, то исходные данные, помимо ручного режима, будут обновляться и автоматически при изменении источника данных, указанного в тэге `<SourceDataConnection>`.

```xml
<ManualRefresh>True</ManualRefresh>
```

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

### AdditionalColumns <a href="#additional_columns" id="additional_columns"></a>

Дополнительные поля элементов дерева. одно поле описывает признак наличия дочерних элементов, другое задает отображаемое значение его состояния (свернут или развернут узел дерева).

```xml
<AdditionalColumns>
  <HasChildrenColumn Name="HasChildren" />
  <StateColumn Name="State" CloseState="+" OpenState="-" />
</AdditionalColumns>
```

Необязательный тэг.

Необязательный тэг `<HasChildrenColumn>`



Если тэг не указан, то для названия поля по умолчанию будет использоваться значение HasChildren.

#### Атрибуты тэга `<HasChildrenColumn>` <a href="#attributes_tag_additional_columns_has_children_column" id="attributes_tag_additional_columns_has_children_column"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="459.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название поля, которое будет использоваться на форме.</p><p></p><p>Обязательный атрибут. Ожидается любое значение.</p></td></tr></tbody></table>

#### Тэг `<StateColumn>` <a href="#additional_columns_state_column" id="additional_columns_state_column"></a>

Элементы дерева.

Необязательный тэг.&#x20;

Если тэг не указан, то по умолчанию: для названия поля будет использоваться значение State, для закрытого состояния отображаемое значение будет "+", а для раскрытого состояния - "-".

#### Атрибуты тэга `<StateColumn>` <a href="#attributes_tag_additional_columns_state_column" id="attributes_tag_additional_columns_state_column"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="459.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название поля, которое будет использоваться на форме.</p><p></p><p>Обязательный атрибут. Ожидается любое значение.</p></td></tr><tr><td align="center">CloseState</td><td><p>Отображаемое значение, если узел свернут.</p><p></p><p>Обязательный атрибут. Ожидается любое значение.</p></td></tr><tr><td align="center">OpenState</td><td><p>Отображаемое значение, если узел раскрыт.</p><p></p><p>Обязательный атрибут. Ожидается любое значение.</p></td></tr></tbody></table>

### Order <a href="#order" id="order"></a>

Сортировка элементов дерева.

Необязательный тэг. Значение тэга `<Order>`: список тэгов `<By>`, отображаемых поле и тип сортировки.

Если правила сортировки не указаны, то используется отображаемое значение элемента (второе обязательное поле) и сортируется по возрастанию.

```xml
<Order>
  <By Name="Title" Type="Asc" />
</Order>
```

### Filter <a href="#filter" id="filter"></a>

Фильтр полученных данных.

{% hint style="info" %}
Фильтрация происходит без изменения источника данных, указанного в тэге `<SourceDataConnection>`.
{% endhint %}

Необязательный тэг.

Может быть двух видов: одиночный фильтр и фильтр-выражение. Подробное описание тэга `<Filter>` доступно по [ссылке](primary_dc/filter.md).

Вариант одиночного фильтра:

```xml
<Filter Type="Equal" FilterByNullValue="True" RefreshFilter="True" Reverse="True">
  <Field NativeName="" />
  <Value></Value>
  <DataType Type="" />
  <Enabled></Enabled>
</Filter>
```

Вариант фильтра-выражения:

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

## Get-проперти для получения свойств <a href="#get_property_tree_get_dc" id="get_property_tree_get_dc"></a>

### ArrayDataByFieldValue <a href="#get_array_data_by_field_value" id="get_array_data_by_field_value"></a>

Возвращает все узлы дерева, найденные по значению FilterValue в поле FilterField.

Результатом будет двумерный массив значений всех полей Fields в тэге [`<SourceDataConnection>`](tree_get_dc.md#source_data_connection) (в порядке объявления) и значение дополнительного поля [`<HasChildrenColumn>`](tree_get_dc.md#additional_columns_has_children_column).

```xml
<DataConnection SourceDataConnection="TreeGetDataConnectionName">
  <Property Name="ArrayDataByFieldValue">
    <Parameters>
      <!--Значение тэга <Parameter> с атрибутом Name, равным FilterField: ожидается название одного из полей-->
      <Parameter Name="FilterField" />
      <!--Значение тэга <Parameter> с атрибутом Name, равным FilterValue: любое значение-->
      <Parameter Name="FilterValue" />
    </Parameters>
  </Property>
</DataConnection>
```

### Ancestor <a href="#get_ancestor" id="get_ancestor"></a>

Возвращает всех предков узла.

Результатом будет двумерный массив значений всех полей Fields в тэге [`<SourceDataConnection>`](tree_get_dc.md#source_data_connection) (в порядке объявления) и значение дополнительного поля [`<HasChildrenColumn>`](tree_get_dc.md#additional_columns_has_children_column).

```xml
<DataConnection SourceDataConnection="TreeGetDataConnectionName">
  <Property Name="Ancestor">
    <Parameters>
      <!--Значение тэга <Parameter>: ожидается целочисленное значение-->
      <Parameter Name="NodeId">1</Parameter>
    </Parameters>
  </Property>
</DataConnection>
```

### Descendant <a href="#get_descendant" id="get_descendant"></a>

Возвращает всех потомков узла.

Результатом будет двумерный массив значений всех полей Fields в тэге [`<SourceDataConnection>`](tree_get_dc.md#source_data_connection) (в порядке объявления) и значение дополнительного поля [`<HasChildrenColumn>`](tree_get_dc.md#additional_columns_has_children_column).

```xml
<DataConnection SourceDataConnection="TreeGetDataConnectionName">
  <Property Name="Descendant">
    <Parameters>
      <!--Значение тэга <Parameter>: ожидается целочисленное значение-->
      <Parameter Name="NodeId">1</Parameter>
    </Parameters>
  </Property>
</DataConnection>
```

### Child <a href="#get_child" id="get_child"></a>

Возвращает дочерние элементы узла.

Результатом будет двумерный массив значений всех полей Fields в тэге [`<SourceDataConnection>`](tree_get_dc.md#source_data_connection) (в порядке объявления) и значение дополнительного поля [`<HasChildrenColumn>`](tree_get_dc.md#additional_columns_has_children_column).

```xml
<DataConnection SourceDataConnection="TreeGetDataConnectionName">
  <Property Name="Child">
    <Parameters>
      <!--Значение тэга <Parameter>: ожидается целочисленное значение-->
      <Parameter Name="NodeId">1</Parameter>
    </Parameters>
  </Property>
</DataConnection>
```

### Parent <a href="#get_parent" id="get_parent"></a>

Возвращает родительский элемент узла.

Результатом будет двумерный массив значений всех полей Fields в тэге [`<SourceDataConnection>`](tree_get_dc.md#source_data_connection) (в порядке объявления) и значение дополнительного поля [`<HasChildrenColumn>`](tree_get_dc.md#additional_columns_has_children_column).

```xml
<DataConnection SourceDataConnection="TreeGetDataConnectionName">
  <Property Name="Parent">
    <Parameters>
      <!--Значение тэга <Parameter>: ожидается целочисленное значение-->
      <Parameter Name="NodeId">1</Parameter>
    </Parameters>
  </Property>
</DataConnection>
```

## Set-проперти для динамического задания свойств <a href="#set_property_tree_get_dc" id="set_property_tree_get_dc"></a>

### ToggleFoldingNode <a href="#set_toggle_folding_node" id="set_toggle_folding_node"></a>

Сворачивание/разворачивание узла.

```xml
<DataConnection SourceDataConnection="TreeGetDataConnectionName">
  <Property Name="ToggleFoldingNode">
    <Parameters>
      <!--Значение тэга <Parameter>: ожидается целочисленное значение-->
      <Parameter Name="NodeId">1</Parameter>
    </Parameters>
  </Property>
</DataConnection>
```

### UpdateNode <a href="#set_update_node" id="set_update_node"></a>

Для элемента с идентификатором NodeId изменяет значения полей FieldNames на значения Values.

```xml
<DataConnection Name="TreeGetDataConnection">
  <Property Name="UpdateNode">
    <Parameters>
      <Parameter Name="NodeId">1</Parameter>
      <Parameter Name="FieldNames">
        <Structure Type="List">
          <Item>FieldName1</Item>
          <Item>FieldName2</Item>
        </Structure>
      </Parameter>
      <Parameter Name="Values">
        <Structure Type="List">
          <Item>Value1</Item>
          <Item>Value2</Item>
        </Structure>
      </Parameter>
    </Parameters>
  </Property>
</DataConnection>
```

### UpdateNodes <a href="#set_update_nodes" id="set_update_nodes"></a>

Для элементов с идентификаторами NodeIds изменяет значения полей FieldNames на значения Values.

```xml
<DataConnection Name="TreeGetDataConnection">
  <Property Name="UpdateNodes">
    <Parameters>
      <Parameter Name="NodeIds">
        <Structure Type="List">
          <Item>1</Item>
          <Item>2</Item>
        </Structure>
      </Parameter>
      <Parameter Name="FieldNames">
        <Structure Type="List">
          <Item>FieldName1</Item>
          <Item>FieldName2</Item>
        </Structure>
      </Parameter>
      <Parameter Name="Values">
        <Structure Type="List">
          <Item>Value1</Item>
          <Item>Value2</Item>
        </Structure>
      </Parameter>
    </Parameters>
  </Property>
</DataConnection>
```
