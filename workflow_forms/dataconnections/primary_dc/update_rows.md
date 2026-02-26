---
description: Подробное описание set-проперти с примерами и пояснениями
---

# UpdateRows

Set-проперти UpdateRows изменяет значения полей GetDataConnection в строках с указанными индексами на соответствующее значение из массива или матрицы.

## Шаблон UpdateRows <a href="#set_update_rows" id="set_update_rows"></a>

```xml
<DataConnection Name="PrimaryGetDataConnectionName">
  <Property Name="UpdateRows">
    <Parameters>
      <Parameter Name="RowIndices"> </Parameter>
      <Parameter Name="ColumnNames"> </Parameter>
      <Parameter Name="Values"> </Parameter>
      <Parameter Name="ReplicateValues">True</Parameter>
      <Parameter Name="RawValues">False</Parameter>
      <Parameter Name="FireChanged">True</Parameter>
    </Parameters>
  </Property>
</DataConnection>
```

### Параметры

#### Параметр **RowIndices**

Обязательный параметр. Массив индексов строк для изменения.\
Ожидает линейный массив неотрицательных целочисленных значений.

#### Параметр **ColumnNames**&#x20;

Обязательный параметр. Массив названий полей для обновления значений.\
Ожидает линейный массив строковых значений.

#### Параметр **Values**&#x20;

Обязательный параметр. Массив или матрица новых значений.\
Ожидает линейный массив или матрицу любых значений.

#### **П**араметр **ReplicateValues**

Необязательный параметр. Признак, определяющий каким образом обрабатывать значение параметра Values.\
Ожидает логическое значение. По умолчанию используется значение True.

Если параметр ReplicateValues имеет значение **False**, то значение **параметра Values** рассматривается **как матрица значений**, которые будут записаны в строки с индексами, указанными в параметре RowIndices. При этом будут соблюдаться правила:

* Если количество элементов строки матрицы не совпадает с количеством полей, указанных в параметре ColumnNames, то в соответствующие ячейки ставится значение NULL;&#x20;
* Если количество строк матрицы не совпадает с количеством индексов, указанных в параметре RowIndices, то в ячейки строк, для которых отсутствуют строки в матрице, ставится значение NULL.

Если параметр ReplicateValues имеет значение **True**, то значение **параметра** **Values** рассматривается **как линейный массив значений**, который заполняет каждую строку, подставляя элементы в соответствующие колонки.

#### Параметр **RawValues**

Необязательный параметр. Признак того, что значения необходимо подставлять "как они есть" - без преобразования в массив скалярных значений.\
Ожидается логическое значение. По умолчанию используется значение False.

#### Параметр **FireChanged**

Необязательный параметр. Признак того, что соединение с данными будет рассылать событие об изменении данных при выполнении set-проперти.\
Ожидается логическое значение. По умолчанию используется значение True.

## Примеры

В примерах будем использовать PrimaryGetDataConnection вида:

```xml
<DataConnection Name="PrimaryGetDataConnection" Type="PrimaryGetDataConnection" Assembly="DataConnections">
  <SqlQuery Name="TestSelectSqlQuery" Type="Select">
    <Workflow Name="Template" />
    <Fields>
      <Field Name="FirstField" />
      <Field Name="SecondField" />
      <Field Name="ThirdField" />
      <Field Name="FourthField" />
    </Fields>
  </SqlQuery>
</DataConnection>
```

В котором будет следующий набор данных:

<figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

### Одно значение в одно поле

Если необходимо _в строках в одно поле_ указать _одинаковое значение_, то в параметре Values достаточно передать _скалярное значение_, а параметру ReplicateValues оставить значение _True_ (по умолчанию).

Пример команды:

```xml
<Command Name="UpdateRowsValueSetCommand" Type="ValueSetCommand" Assembly="Commands">
  <DataConnection Name="PrimaryGetDataConnection">
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
            <Item>FourthField</Item>
          </Structure>
        </Parameter>
        <Parameter Name="Values">99</Parameter>
        <Parameter Name="ReplicateValues">True</Parameter>
      </Parameters>
    </Property>
  </DataConnection>
</Command>
```

В этом случае получим:

<figure><img src="../../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

### Разные значение в одно поле

Если необходимо в строках _в одно поле_ указать _разные значения_, то в параметре Values необходимо передавать _матрицу значений_ (таблицу), а параметру ReplicateValues задавать значение _False_.

Пример команды:

```xml
<Command Name="UpdateRowsValueSetCommand" Type="ValueSetCommand" Assembly="Commands">
  <DataConnection Name="PrimaryGetDataConnection">
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
            <Item>FourthField</Item>
          </Structure>
        </Parameter>
        <Parameter Name="Values">
          <Structure Type="Table">
            <Row>
              <Item>99</Item>
            </Row>
            <Row>
              <Item>98</Item>
            </Row>
          </Structure>
        </Parameter>
        <Parameter Name="ReplicateValues">False</Parameter>
      </Parameters>
    </Property>
  </DataConnection>
</Command>
```

В этом случае получим:

<figure><img src="../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

#### Как не правильно&#x20;

Если в параметре Values передадим _массив значений_ и параметру ReplicateValues оставим значение по умолчанию (True), то в каждую строку будет подставлено одно и тоже значение - первый элемент массива. Остальные элементы массива будут отброшены.



Если в параметре Values передадим _массив значений_ при этом для параметра ReplicateValues укажем значение _False_, то массив значений будет преобразован в _матрицу из одной строки_ с элементами исходного массива. Заменится значение поля только первой строки первым элементом исходного массива. В остальных строках будет подставлено значение NULL. Сработало правило:

> Если количество строк матрицы не совпадает с количеством индексов, указанных в параметре RowIndices, то в ячейки строк, для которых отсутствуют строки в матрице, ставится значение NULL.

Пример команды:

```xml
<Command Name="UpdateRowsValueSetCommand" Type="ValueSetCommand" Assembly="Commands">
  <DataConnection Name="PrimaryGetDataConnection">
    <Property Name="UpdateRows">
      <Parameters>
        <Parameter Name="RowIndices">
          <Structure Type="List">
            <Item>1</Item>
            <Item>2</Item>
            <Item>4</Item>
          </Structure>
        </Parameter>
        <Parameter Name="ColumnNames">
          <Structure Type="List">
            <Item>FourthField</Item>
          </Structure>
        </Parameter>
        <Parameter Name="Values">
          <Structure Type="List">
            <Item>99</Item>
            <Item>98</Item>
            <Item>97</Item>
          </Structure>
        </Parameter>
        <Parameter Name="ReplicateValues">False</Parameter>
      </Parameters>
    </Property>
  </DataConnection>
</Command>
```

В этом случае получим:

<figure><img src="../../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

### Одинаковые значения в разные строки

Если необходимо в строках _в несколько полей_ задать _одинаковые значения_, то в параметре Values необходимо передать _массив значений_ и параметру ReplicateValues оставить значение _True_ (по умолчанию). Тогда значения из массива будут подставлены в каждую строку.

Пример команды:

```xml
<Command Name="UpdateRowsValueSetCommand" Type="ValueSetCommand" Assembly="Commands">
  <DataConnection Name="PrimaryGetDataConnection">
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
            <Item>SecondField</Item>
            <Item>FourthField</Item>
          </Structure>
        </Parameter>
        <Parameter Name="Values">
          <Structure Type="List">
            <Item>New text</Item>
            <Item>99</Item>
          </Structure>
        </Parameter>
        <Parameter Name="ReplicateValues">True</Parameter>
      </Parameters>
    </Property>
  </DataConnection>
</Command>
```

В этом случае получим:

<figure><img src="../../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

### Разные значения в разные строки

Если необходимо в строках _в несколько полей_ задать _разные значения_, то в параметре Values необходимо передать _матрицу значений_ и параметру ReplicateValues задать значение _False_. Тогда значения из матрицы будут построчно подставлены в соответствующую строку в порядке перечисления индексов и значений в матрице.

Пример команды:

```xml
<Command Name="UpdateRowsValueSetCommand" Type="ValueSetCommand" Assembly="Commands">
  <DataConnection Name="PrimaryGetDataConnection">
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
            <Item>SecondField</Item>
            <Item>FourthField</Item>
          </Structure>
        </Parameter>
        <Parameter Name="Values">
          <Structure Type="Table">
            <Row>
              <Item>New text</Item>
              <Item>99</Item>
            </Row>
            <Row>
              <Item>Other text</Item>
              <Item>98</Item>
            </Row>
          </Structure>
        </Parameter>
        <Parameter Name="ReplicateValues">False</Parameter>
      </Parameters>
    </Property>
  </DataConnection>
</Command>
```

В этом случае получим:

<figure><img src="../../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Если в этом примере для параметра ReplicateValues оставим значение True (по умолчанию), то матрица значений:

```
+--------------+------+
|  New text    |  99  |
|  Other text  |  98  |
+--------------+------+
```

преобразуется в линейный массив:

```
+------------+--------------+
|  New text  |  Other text  |
+------------+--------------+
```

Такая команда будет вставлять в каждую строку одинаковые значения. Если тип колонки не совпадает с типом вставляемого значений, то команда выбросит ошибку System.FormatException.
{% endhint %}





### `<Array>` в качестве источника данных





\<Array> возвращает таблицу (матрицу)

```xml
<Command Name="UpdateRowsValueSetCommand" Type="ValueSetCommand" Assembly="Commands">
  <DataConnection Name="PrimaryGetDataConnection">
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
            <Item>SecondField</Item>
            <Item>FourthField</Item>
          </Structure>
        </Parameter>
        <Parameter Name="Values">
          <Array>
            <Source>
              <Structure Type="Table">
                <Row>
                  <Item>New text</Item>
                  <Item>99</Item>
                </Row>
                <Row>
                  <Item>Some text</Item>
                  <Item>50</Item>
                </Row>
                <Row>
                  <Item>Other text</Item>
                  <Item>98</Item>
                </Row>
              </Structure>
            </Source>
            <Filter Type="Greater">
              <Index Value="1" />
              <Value>55</Value>
            </Filter>
          </Array>
        </Parameter>
        <Parameter Name="ReplicateValues">False</Parameter>
      </Parameters>
    </Property>
  </DataConnection>
</Command>
```





Если в ячейках таблицы храниться массив. А такое возможно?

