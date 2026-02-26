---
description: >-
  Вторично загружающее соединение с данными. Получает данные из другого
  загружающего соединения с данными и фильтрует их без изменения источника.
---

# SecondaryGetDataConnection

## Шаблон SecondaryGetDataConnection <a href="#template_secondary_dc" id="template_secondary_dc"></a>

```xml
<DataConnection Name="" Type="SecondaryGetDataConnection" Assembly="DataConnections">
  <SourceDataConnection Name="" SqlQuery="" />
  <ManualRefresh></ManualRefresh> 
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
  <StartPosition></StartPosition>
  <MaxCount></MaxCount>
</DataConnection>
```

## Описание SecondaryGetDataConnection <a href="#description_secondary_dc" id="description_secondary_dc"></a>

```xml
<DataConnection Name="SecondaryGetDataConnectionName" Type="SecondaryGetDataConnection" Assembly="DataConnections">
  <!--Тэги, специфичные для SecondaryGetDataConnection-->
</DataConnection>
```

## Тэги, специфичные для SecondaryGetDataConnection <a href="#tags_secondary_dc" id="tags_secondary_dc"></a>

### SourceDataConnection <a href="#source_data_connection" id="source_data_connection"></a>

Загружающее соединение с данными, которое будет источником данных для фильтрации.

```xml
<SourceDataConnection Name="SourceDataConnectionName" SqlQuery="SqlQueryName" />
```

Обязательный тэг. Значение тэга не ожидается.

Обязательный атрибут `Name` - имя загружающего соединения с данными. Ожидается имя одного из загружающих соединений с данными, описанных в форме.

Необязательный атрибут `SqlQuery` - имя запроса из загружающего соединения с данными, если в качестве источника данных указан [PrimaryGetDataConnection](primary_dc/) с несколькими запросами SqlQuery. Ожидается имя одного из запросов из загружающего соединения с данными.

{% hint style="info" %}
Если в качестве источника данных используется PrimaryGetDataConnection с несколькими запросами и не указан атрибут `SqlQuery` с именем конкретного запроса, то SecondaryGetDataConnection будет использовать результат запроса первого в порядке описания в синтаксисе PrimaryGetDataConnection.
{% endhint %}

### ManualRefresh <a href="#manual_refresh" id="manual_refresh"></a>

Признак, определяющий условия обновления полученных данных. Если значение True, то обновление будет происходить только в ручном режиме при выполнении команды [DataConnectionRefreshCommand](../commands/dc_refresh_command.md). Если значение False, то исходные данные, помимо ручного режима, будут обновляться и автоматически при изменении источника данных, указанного в тэге `<SourceDataConnection>`.

```xml
<ManualRefresh>True</ManualRefresh>
```

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

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

### StartPosition <a href="#start_position" id="start_position"></a>

Номер строки (отсчет начинается с 1), начиная с которой данные будут входить в результирующую таблицу текущего вторичного соединения с данными.

```xml
<StartPosition>1</StartPosition>
```

Необязательный тэг. Ожидается положительное целочисленное значение.

Пустое значение или значение меньше 1 соответствуют тому, что строки будут выведены начиная с 1-ой.

По умолчанию используется значение 0.

### MaxCount <a href="#max_count" id="max_count"></a>

Максимальное количество строк, которые будут входить в результирующую таблицу текущего вторичного соединения с данными.

```xml
<MaxCount>100</MaxCount>
```

Необязательный тэг. Ожидается положительное целочисленное значение.

Пустое значение или значение меньше 0 соответствуют тому, что ограничения по количеству строк нет.

По умолчанию используется значение -1.

## Get-проперти для получения свойств <a href="#get_property_primary_dc" id="get_property_primary_dc"></a>

### Count <a href="#get_count" id="get_count"></a>

Возвращает количество строк во вторичном загружающем соединении с данными.

```xml
<DataConnection SourceDataConnection="SecondaryGetDataConnectionName">
  <Property Name="Count"/>
</DataConnection>
```

Значение не ожидается.

### ValueChanged <a href="#get_value_changed" id="get_value_changed"></a>

Возвращает признак изменения данных DataConnection.

```xml
<DataConnection SourceDataConnection="SecondaryGetDataConnectionName">
  <Property Name="ValueChanged" />
</DataConnection>
```

Значение не ожидается.

### RowIndexOf <a href="#get_row_index_of" id="get_row_index_of"></a>

Возвращает индекс строки, удовлетворяющей условиям соответствия названий столбцов и значений в этих столбцах.

```xml
<DataConnection SourceDataConnection="SecondaryGetDataConnectionName">
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
<DataConnection SourceDataConnection="SecondaryGetDataConnectionName">
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
<DataConnection SourceDataConnection="SecondaryGetDataConnectionName">
  <Property Name="Column">
    <Parameters>
      <Parameter Name="ColumnName">ColumnName</Parameter>
    </Parameters>
  </Property>  
</DataConnection>
```

Параметр **ColumnName** ожидает название одного из полей DataConnection.

## Set-проперти для динамического задания свойств

### AddRow <a href="#set_add_row" id="set_add_row"></a>

Добавляет новую строку в таблицу DataConnection.

```xml
<DataConnection Name="SecondaryGetDataConnectionName">
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
<DataConnection Name="SecondaryGetDataConnectionName">
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
<DataConnection Name="SecondaryGetDataConnectionName">
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
<DataConnection Name="SecondaryGetDataConnectionName">
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

Если параметр ReplicateValues имеет значение _False_, то значение параметра Values рассматривается как _матрица значений_, которые будут записаны в строки с индексами, указанными в параметре RowIndices. При этом:

* Если количество элементов строки матрицы не совпадает с количеством полей, указанных в параметре ColumnNames, то в соответствующие ячейки ставится значение NULL;&#x20;
* Если количество строк матрицы не совпадает с количеством индексов, указанных в параметре RowIndices, то в ячейки строк, для которых отсутствуют строки в матрице, ставится значение NULL.

Если параметр ReplicateValues имеет значение _True_, то значение параметра Values рассматривается как _линейный массив значений_, который заполняет каждую строку, подставляя элементы в соответствующие колонки.

Необязательный параметр **RawValues** - признак того, что значения необходимо подставлять "как они есть" - без преобразования в массив скалярных значений. Ожидается логическое значение. По умолчанию используется значение False.

Необязательный параметр **FireChanged** - признак того, что соединение с данными будет рассылать событие об изменении данных при выполнении set-проперти. Ожидается логическое значение. По умолчанию используется значение True.

### UpdateColumn <a href="#set_update_column" id="set_update_column"></a>

Построчно изменяет значения строк в заданном поле на соответствующие значения из массива.

```xml
<DataConnection Name="SecondaryGetDataConnectionName">
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
<DataConnection Name="SecondaryGetDataConnectionName">
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
<DataConnection Name="SecondaryGetDataConnectionName">
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

```xml
<DataConnection Name="SecondaryGetDataConnectionName">
  <Property Name="FireChanged" />
</DataConnection>
```

Значение не ожидается.

### ValueChanged <a href="#set_value_changed" id="set_value_changed"></a>

Задает признак изменения значения соединения с данными.

```xml
<DataConnection Name="SecondaryGetDataConnectionName">
  <Property Name="ValueChanged">False</Property>
</DataConnection>
```

Ожидается логическое значение.
