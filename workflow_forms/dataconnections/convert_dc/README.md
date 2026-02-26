---
description: >-
  Преобразующее загружающее соединение с данными; получает данные из другого
  загружающего соединения с данными и фильтрует их.
---

# ConvertDataConnection

## Шаблон ConvertDataConnection <a href="#template" id="template"></a>

```xml
<DataConnection Name="" Type="ConvertDataConnection" Assembly="WorkflowServer">
  <SourceDataConnection Name="" Query=""/>
  <ManualRefresh></ManualRefresh>
  <Fields>
    <Field Name="" Field=""/>
    <Field Field="" Type="Object">
      <Field Name="" />
    </Field>
    <Field Name="" Type="SubField" SubField="" Field=""/>
    <Field Name="" Field="" Type="Array">
      <Field Name="" />
    </Field>
    <Field Name="" Type="Value" DataType=""></Field>
    <Field Name="" Type="Format"></Field>
    <Field Name="" Type="Substitution" Field=""></Field>
    <Field Name="" Type="Replace" Field=""></Field>
    <Field Name="" Type="Action" Field=""></Field>
    <Field Name="" Type="TemplateFormat" Evaluate=""></Field>
  </Fields>
  <Filter>
    <And RefreshFilter="">
      <Or RefreshFilter="">
        <Filter Type="" FilterByNullValue="" RefreshFilter="" Reverse="">
          <Field NativeName="" />
          <Value></Value>
          <DataType Type="" />
          <Enabled>True</Enabled>
        </Filter>
        <Filter Type="" FilterByNullValue="" RefreshFilter="" Reverse="">
          <Field NativeName="" />
          <Value></Value>
          <DataType Type="" />
          <Enabled>True</Enabled>
        </Filter>
      </Or>
      <Not RefreshFilter="">
        <Filter Type="" FilterByNullValue="" RefreshFilter="" Reverse="">
          <Field NativeName="" />
          <Value></Value>
          <DataType Type="" />
          <Enabled>True</Enabled>
        </Filter>
      </Not>
    </And>
  </Filter>
  <Order>
    <By Name="" Type="" />
  </Order>
</DataConnection>
```

## Описание ConvertDataConnection <a href="#description" id="description"></a>

```xml
<DataConnection Name="ConvertDataConnectionName" Type="ConvertDataConnection" Assembly="DataConnections">
  <!--Тэги, специфичные для ConvertDataConnection-->
</DataConnection>
```

## Тэги, специфичные для ConvertDataConnection <a href="#specific-tags" id="specific-tags"></a>

### SourceDataConnection <a href="#source_data_connection" id="source_data_connection"></a>

Загружающее соединение с данными, которое будет источником данных для преобразования и фильтрации.

Обязательный тэг. Значение тэга не ожидается.

```xml
<SourceDataConnection Name="SourceDataConnectionName" Query="SqlQueryName" />
```

Обязательный атрибут `Name` - имя загружающего соединения с данными. Ожидается имя одного из загружающих соединений с данными, описанных на форме.

Необязательный атрибут `Query` - имя запроса из загружающего соединения с данными, если в качестве источника данных указан [PrimaryGetDataConnection](../primary_dc/) с несколькими запросами SqlQuery. Ожидается имя одного из запросов из загружающего соединения с данными.

{% hint style="info" %}
Если в качестве источника данных используется PrimaryGetDataConnection с несколькими запросами и не указан атрибут `SqlQuery` с именем конкретного запроса, то ConvertDataConnection будет использовать результат запроса первого в порядке описания в синтаксисе PrimaryGetDataConnection.
{% endhint %}

### ManualRefresh <a href="#manual_refresh" id="manual_refresh"></a>

Признак, определяющий условия обновления полученных данных.\
Если значение True, то обновление будет происходить только в ручном режиме при выполнении команды [DataConnectionRefreshCommand](../../commands/dc_refresh_command.md). Если значение False, то исходные данные, помимо ручного режима, будут обновляться и автоматически при изменении источника данных, указанного в тэге `<SourceDataConnection>`.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<ManualRefresh>True</ManualRefresh>
```

### Fields <a href="#fields" id="fields"></a>

Список селекторов для выбора колонок из соединения с данными, указанного в тэге `<SourceDataConnection>`, и добавления новых.

Обязательный тэг. Ожидается список тэгов [`<Field>`](selectors.md), содержащих описание селекторов.

```xml
<Fields>
  <Field Name="FieldName" Field="SourceFieldName"/>
  <Field Field="FieldName" Type="Object">
    <Field Name="SubFieldName" />
  </Field>
  <Field Name="FieldName" Type="SubField" Field="FieldName" SubField="SubFieldName"/>
  <Field Name="FieldName" Type="Array" Field="FieldName">
    <Field Name="FieldName" />
  </Field>
  <Field Name="FieldName" Type="Value" DataType="StringDataType">Value</Field>
  <Field Name="FieldName" Type="Format">{FieldName}</Field>
  <Field Name="FieldName" Type="Substitution" Field="FieldName"></Field>
  <Field Name="FieldName" Type="Replace" Field="FieldName"></Field>
  <Field Name="FieldName" Type="Action" Field="FieldName">Array Operations</Field>
  <Field Name="FieldName" Type="TemplateFormat" Evaluate="True">Template</Field>
</Fields>
```

Селекторы в порядке объявления преобразуют каждую строку исходного соединения с данными.

Поддерживаются селекторы следующих типов:

* [Field](selectors.md#selector_field) - Поле соединения с данными;
* [Object](selectors.md#selector_object) - Поля объекта;
* [SubField](selectors.md#selector_sub_field) - Вложенное поле объекта;
* [Array](selectors.md#selector_array) - Соединение массивов объектов;
* [Value](selectors.md#selector_value) - Значение;
* [Format](selectors.md#selector_format) - Форматирование строки;
* [Substitution](selectors.md#selector_substitution) - Подстановка значений;
* [Replace](selectors.md#selector_replace) - Замена значений;
* [Action](selectors.md#selector_action) - Работа с массивами;
* [TemplateFormat](selectors.md#selector_template_format) - Форматирование строки по шаблону.

Тип селектора определяется обязательным атрибутом `Type`.

### Filter <a href="#filter" id="filter"></a>

Фильтр полученных данных.

Необязательный тэг.

{% hint style="info" %}
Фильтрация происходит без изменения источника данных, указанного в тэге `<SourceDataConnection>`.
{% endhint %}

Может быть двух видов: одиночный фильтр и фильтр-выражение. Подробное описание тэга `<Filter>` доступно по [ссылке](../primary_dc/filter.md).

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

### Order

Сортировка данных.

Необязательный тэг. Ожидает список тэгов `<By>`.

Тэг `<By>` имеет два обязательных атрибута: `Name` - имя поля сортировки, и `Type` - направление сортировки (Asc или Desc).

```xml
<Order>
  <By Name="FieldName" Type="Asc" />
</Order>
```

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### Count <a href="#get_count" id="get_count"></a>

Возвращает количество строк в преобразующем загружающем соединении с данными.

```xml
<DataConnection SourceDataConnection="ConvertDataConnectionName">
  <Property Name="Count"/>
</DataConnection>
```

### ValueChanged <a href="#get_value_changed" id="get_value_changed"></a>

Возвращает признак изменения данных DataConnection.

```xml
<DataConnection SourceDataConnection="ConvertDataConnectionName">
  <Property Name="ValueChanged" />
</DataConnection>
```

### RowIndexOf <a href="#get_row_index_of" id="get_row_index_of"></a>

Возвращает индекс строки, удовлетворяющей условиям соответствия названий столбцов и значений в этих столбцах.

```xml
<DataConnection SourceDataConnection="ConvertDataConnectionName">
  <Property Name="RowIndexOf">
    <Parameters>
      <Parameter Name="ColumnNames">
        <Structure Type="List">
          <Item>ColumnName1</Item>
          <Item>ColumnName2</Item>
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

Параметр **ColumnNames** ожидает линейный массив названий полей DataConnection.

Параметр **Values** ожидает линейный массив любых значений, по которым будет произведен поиск в соответствующих полях.

### RowsIndicesOf <a href="#get_rows_indices_of" id="get_rows_indices_of"></a>

Возвращает массив индексов строки, удовлетворяющих условиям соответствия названий столбцов и значений в этих столбцах.

```xml
<DataConnection SourceDataConnection="ConvertDataConnectionName">
  <Property Name="RowsIndicesOf">
    <Parameters>
      <Parameter Name="ColumnNames">
        <Structure Type="List">
          <Item>ColumnName1</Item>
          <Item>ColumnName2</Item>
        </Structure>
      </Parameter>
      <Parameter Name="Values">
        <Structure Type="List">
          <Item>Value1</Item>
          <Item>
            <Structure Type="List">
              <Item>Value2</Item>
              <Item>Value3</Item>
            </Structure>
          </Item>
        </Structure>
      </Parameter>
      <Parameter Name="SearchWithArrays">False</Parameter>
    </Parameters>
  </Property>
</DataConnection>
```

Параметр **ColumnNames** ожидает линейный массив названий полей DataConnection.

Параметр **Values** ожидает линейный массив любых значений, по которым будет произведен поиск в соответствующих полях.

Необязательный параметр **SearchWithArrays** разрешает для каждого столбца использовать линейный массив значений, с элементами которого будет сравниваться значения из каждой строки соответствующего столбца. Ожидается логическое значение. По умолчанию используется значение False.

### Column

Возвращает линейный массив значений, содержащихся в определенном столбце таблицы.

```xml
<DataConnection SourceDataConnection="ConvertDataConnectionName">
  <Property Name="Column">
    <Parameters>
      <Parameter Name="ColumnName">ColumnName</Parameter>
    </Parameters>
  </Property>  
</DataConnection>
```

Параметр **ColumnName** ожидает название одного из полей DataConnection.

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

### AddRow <a href="#set_add_row" id="set_add_row"></a>

Добавляет новую строку в таблицу DataConnection.

```xml
<DataConnection Name="ConvertDataConnectionName">
  <Property Name="AddRow">
    <Parameters>
      <Parameter Name="ColumnNames">
        <Structure Type="List">
          <Item>ColumnName1</Item>
          <Item>ColumnName2</Item>
        </Structure>
      </Parameter>
      <Parameter Name="Values">
        <Structure Type="List">
          <Item>Value1</Item>
          <Item>Value2</Item>
        </Structure>
      </Parameter>
      <Parameter Name="Index">0</Parameter>
      <Parameter Name="FireChanged">False</Parameter>
    </Parameters>
  </Property>
</DataConnection>
```

Параметр **ColumnNames** ожидает линейный массив названий полей DataConnection.

Параметр **Values** ожидает линейный массив любых значений, которые будут записаны в соответствующие поля новой строки.

Необязательный параметр **Index** ожидает неотрицательное целочисленное значение, указывающее место вставки новой строки. Если параметр отсутствует, то строка добавляется в конец таблицы DataConnection.

Необязательный параметр **FireChanged** - признак того, что соединение с данными будет рассылать событие об изменении данных при выполнении set-проперти. Ожидается логическое значение. По умолчанию используется значение True.

### AddRows <a href="#set_add_rows" id="set_add_rows"></a>

Добавляет новые строки в таблицу DataConnection.

```xml
<DataConnection Name="ConvertDataConnectionName">
  <Property Name="AddRows">
    <Parameters>
      <Parameter Name="ColumnNames">
        <Structure Type="List">
          <Item>ColumnName1</Item>
          <Item>ColumnName2</Item>
        </Structure>
      </Parameter>
      <Parameter Name="Values">
        <DataConnection SourceDataConnection="SourceDataConnectionName">
          <Fields>
            <Field Name="ColumnName1" />
            <Field Name="ColumnName2" />
          </Fields>
        </DataConnection>
      </Parameter>
      <Parameter Name="Index">0</Parameter>
      <Parameter Name="RawValues">True</Parameter>
      <Parameter Name="FireChanged">False</Parameter>
    </Parameters>
  </Property>
</DataConnection>
```

Параметр **ColumnNames** ожидает линейный массив названий полей DataConnection.

Параметр **Values** ожидает таблицу (например, ссылка на GetDataConnection) с числом столбцов равным числу имен столбцов, указанных в параметре ColumnNames. Допустимо указывать линейный массив, который будет соответствовать одной строке.

Необязательный параметр **Index** ожидает неотрицательное целочисленное значение, указывающее место вставки новой строки. Если параметр отсутствует, то строка добавляется в конец таблицы DataConnection.

Необязательный параметр **RawValues** - признак того, что значения необходимо подставлять "как они есть" - без преобразования в массив скалярных значений. Ожидается логическое значение. По умолчанию используется значение False.

Необязательный параметр **FireChanged** - признак того, что соединение с данными будет рассылать событие об изменении данных при выполнении set-проперти. Ожидается логическое значение. По умолчанию используется значение True.

### UpdateRow <a href="#set_update_row" id="set_update_row"></a>

Изменяет значения полей в строке с указанным индексом.

```xml
<DataConnection Name="ConvertDataConnectionName">
  <Property Name="UpdateRow">
    <Parameters>
      <Parameter Name="RowIndex">0</Parameter>
      <Parameter Name="ColumnNames">
        <Structure Type="List">
          <Item>ColumnName1</Item>
          <Item>ColumnName2</Item>
        </Structure>
      </Parameter>
      <Parameter Name="Values">
        <Structure Type="List">
          <Item>Value1</Item>
          <Item>Value2</Item>
        </Structure>
      </Parameter>
      <Parameter Name="RawValues">True</Parameter>
      <Parameter Name="FireChanged">False</Parameter>
    </Parameters>
  </Property>
</DataConnection>
```

Параметр **ColumnNames** ожидает линейный массив названий полей DataConnection.

Параметр **Values** ожидает линейный массив любых значений.

Параметр **RowIndex** ожидает неотрицательное целочисленное значение, указывающее на индекс строки для изменения.

Необязательный параметр **RawValues** - признак того, что значения необходимо подставлять "как они есть" - без преобразования в массив скалярных значений. Ожидается логическое значение. По умолчанию используется значение False.

Необязательный параметр **FireChanged** - признак того, что соединение с данными будет рассылать событие об изменении данных при выполнении set-проперти. Ожидается логическое значение. По умолчанию используется значение True.

### UpdateRows <a href="#set_update_rows" id="set_update_rows"></a>

Изменяет значения полей в строках с указанными индексами на соответствующее значение из массива.

```xml
<DataConnection Name="ConvertDataConnectionName">
  <Property Name="UpdateRows">
    <Parameters>
      <Parameter Name="RowIndices">
        <Structure Type="List">
          <Item>1</Item>
          <Item>2</Item>
        </Structure>
      </Parameter>
      <Parameter Name="ColumnNames">
        <Structure Type="List">
          <Item>ColumnName1</Item>
          <Item>ColumnName2</Item>
        </Structure>
      </Parameter>
      <Parameter Name="Values">
        <Structure Type="List">
          <Item>Value1</Item>
          <Item>Value2</Item>
        </Structure>
      </Parameter>
      <Parameter Name="ReplicateValues">False</Parameter>
      <Parameter Name="RawValues">True</Parameter>
      <Parameter Name="FireChanged">False</Parameter>
    </Parameters>
  </Property>
</DataConnection>
```

Параметр **ColumnNames** ожидает линейный массив названий полей DataConnection.

Параметр **Values** ожидает линейный массив или матрицу любых значений.

Параметр **RowIndices** ожидает линейный массив неотрицательных целочисленных значений, указывающих на индексы строк для изменения.

Необязательный параметр **ReplicateValues** - признак, определяющий каким образом обрабатывать значение параметра Values. Ожидает логическое значение. По умолчанию используется значение True.

Если значение параметра _False_, то значение параметра Values рассматривается как _матрица значений_, которые будут записаны в строки с индексами, указанными в параметре RowIndices. При этом:

* если количество элементов строки матрицы не совпадает с количеством полей, указанных в параметре ColumnNames, то в соответствующие ячейки ставится значение NULL;&#x20;
* если количество строк матрицы не совпадает с количеством индексов, указанных в параметре RowIndices, то в ячейки строки, у которых отсутствует строка в матрице, ставится значение NULL.

Если значение параметра _True_, то значение параметра Values рассматривается как _линейный массив значений_, который заполняет каждую строку, подставляя элементы в соответствующие колонки.

Необязательный параметр **RawValues** - признак того, что значения необходимо подставлять "как они есть" - без преобразования в массив скалярных значений. Ожидается логическое значение. По умолчанию используется значение False.

Необязательный параметр **FireChanged** - признак того, что соединение с данными будет рассылать событие об изменении данных при выполнении set-проперти. Ожидается логическое значение. По умолчанию используется значение True.

### UpdateColumn <a href="#set_update_column" id="set_update_column"></a>

Построчно изменяет значения строк в заданном поле на соответствующие значения из массива.

```xml
<DataConnection Name="ConvertDataConnectionName">
  <Property Name="UpdateColumn">
    <Parameters>
      <Parameter Name="ColumnName">ColumnName</Parameter>
      <Parameter Name="Values">
        <Structure Type="List">
          <Item>Value1</Item>
          <Item>Value2</Item>
        </Structure>
      </Parameter>
      <Parameter Name="RawValues">True</Parameter>
      <Parameter Name="FireChanged">False</Parameter>
    </Parameters>
  </Property>
</DataConnection>
```

Параметр **ColumnName** ожидает название поля DataConnection.

Параметр **Values** ожидает линейный массив любых значений. Если длина массива меньше количества строк в соединении с данными, то оставшиеся строки не будут изменяться. Если длина массива больше, то оставшиеся значения будут отброшены.

Необязательный параметр **RawValues** - признак того, что значения необходимо подставлять "как они есть" - без преобразования в массив скалярных значений. Ожидается логическое значение. По умолчанию используется значение False.

Необязательный параметр **FireChanged** - признак того, что соединение с данными будет рассылать событие об изменении данных при выполнении set-проперти. Ожидается логическое значение. По умолчанию используется значение True.

### UpdateColumnCellsValues <a href="#set_update_column_cells_values" id="set_update_column_cells_values"></a>

Изменяет значение поля в строках с указанными индексами на заданное значение.

```xml
<DataConnection Name="ConvertDataConnectionName">
  <Property Name="UpdateColumnCellsValues">
    <Parameters>
      <Parameter Name="ColumnName">ColumnName</Parameter>
      <Parameter Name="RowIndices">
        <Structure Type="List">
          <Item>1</Item>
          <Item>2</Item>
        </Structure>
      </Parameter>
      <Parameter Name="Value">Value</Parameter>
      <Parameter Name="RawValues">True</Parameter>
      <Parameter Name="FireChanged">False</Parameter>
    </Parameters>
  </Property>
</DataConnection>
```

Параметр **ColumnName** ожидает название поля DataConnection.

Параметр **Value** ожидает значение, которое будет подставляться в поле.

Необязательный параметр **RowIndices** ожидает линейный массив неотрицательных целочисленных значений, указывающих на индексы строк. Если параметр не указан, то обновятся все строки.

Необязательный параметр **FireChanged** - признак того, что соединение с данными будет рассылать событие об изменении данных при выполнении set-проперти. Ожидается логическое значение. По умолчанию используется значение True.

### DeleteRowsByIndices <a href="#set_delete_rows_by_indices" id="set_delete_rows_by_indices"></a>

Удаляет строки с указанными индексами.

```xml
<DataConnection Name="ConvertDataConnectionName">
  <Property Name="UpdateColumnCellsValues">
    <Parameters>
      <Parameter Name="Value">
        <Structure Type="List">
          <Item>1</Item>
          <Item>2</Item>
        </Structure>
      </Parameter>
      <Parameter Name="FireChanged">False</Parameter>
    </Parameters>
  </Property>
</DataConnection>
```

Необязательный параметр **Value** ожидает линейный массив неотрицательных целочисленных значений. Если параметр отсутствует, то удаляются все строки.

Необязательный параметр **FireChanged** - признак того, что соединение с данными будет рассылать событие об изменении данных при выполнении set-проперти, а так же будет изменяться свойство ValueChanged. Ожидается логическое значение. По умолчанию используется значение True.

### FireChanged <a href="#set_fire_changed" id="set_fire_changed"></a>

Рассылает событие об изменении данных.

Значение не ожидается.

```xml
<DataConnection Name="ConvertDataConnectionName">
  <Property Name="FireChanged" />
</DataConnection>
```

### ValueChanged <a href="#set_value_changed" id="set_value_changed"></a>

Задает признак изменения значения соединения с данными.

Ожидается логическое значение.

```xml
<DataConnection Name="ConvertDataConnectionName">
  <Property Name="ValueChanged">False</Property>
</DataConnection>
```
