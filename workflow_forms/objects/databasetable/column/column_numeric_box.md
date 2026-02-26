---
description: >-
  Используется для отображения числовых значений и предоставляет пользователю
  возможностью задавать значение через NumericBox, если в таблице разрешено
  редактирование
---

# ColumnNumericBox

## Шаблон DatabaseTableColumnNumericBox <a href="#template_databasetable" id="template_databasetable"></a>

Перечень всех возможных тэгов столбца:

```xml
<Column Name="" Type="DatabaseTableColumnNumericBox" Assembly="DatabaseTableColumnControls" >
  <!--Тэги, общие для всех типов столбцов-->
  <Title></Title>
  <Width></Width>
  <MinimumWidth></MinimumWidth>
  <DisplayIndex></DisplayIndex>
  <Frozen Value="" />
  <WrapMode Value="" />
  <ReadOnly></ReadOnly> 
  <AllowSort Value="" />
  <Alignment Value="" />
  <HeaderAlignment Value="" />
  <AutoSizeMode Value="" />
  <HeaderBackColor></HeaderBackColor>
  <HeaderForeColor></HeaderForeColor>
  <BackColor></BackColor>
  <ForeColor></ForeColor>
  <Visible></Visible>
  <Hint></Hint>
  <DataType DataType="" />
  <Substitution SourceColumn="">
    <DataConnection SourceDataConnection="">
      <Fields>
        <Field Name="" />
        <Field Name="" />
      </Fields>
    </DataConnection>
  </Substitution>
  <Sorting>
    <SortOrder Type="" />
    <ColumnOrder Order="" />
  </Sorting>
  <Filter AutoFill="" FilterNullValue=""></Filter>
  <DefaultNewRowValue></DefaultNewRowValue>
  <AutoFill Type="" />
  <Calculate>
    <Expression></Expression>
    <Items>
      <Item></Item>
      <Item></Item>
    </Items>
  </Calculate>
  <ManagementMode></ManagementMode>
  <!--Тэги, специфичные для DatabaseTableColumnNumericBox-->
  <Increment Value="" />
  <Maximum Value="" />
  <Minimum Value="" />
  <DecimalPlaces Value="" />
  <ThousandsSeparator Value="" />
</Column>
```

{% hint style="info" %}
Тэги, общие для всех типов столбцов описаны в статье [Column](./).
{% endhint %}

## Тэги, специфичные для столбцов типа DatabaseTableColumnNumericBox <a href="#column_combo_box_tags" id="column_combo_box_tags"></a>

### Increment <a href="#column_increment" id="column_increment"></a>

Число, на которое будет изменяться значение поля.

```xml
<Increment Value="1" />
```

Необязательный тэг. Значение тэга не ожидается.&#x20;

Обязательный атрибут `Value` ожидает числовое значение. По умолчанию используется значение 1.

### Maximum <a href="#column_maximum" id="column_maximum"></a>

Максимальное допустимое число для ввода.&#x20;

```xml
<Maximum Value="100" />
```

Необязательный тэг. Значение тэга не ожидается.&#x20;

Обязательный атрибут `Value` ожидает числовое значение. По умолчанию используется значение 100.

### Minimum <a href="#column_minimum" id="column_minimum"></a>

Минимальное допустимое число для ввода.

```xml
<Minimum Value="0" />
```

Необязательный тэг. Значение тэга не ожидается.&#x20;

Обязательный атрибут `Value` ожидает числовое значение. По умолчанию используется значение 0.

### DecimalPlaces <a href="#column_decimal_places" id="column_decimal_places"></a>

Количество знаков дробной части числа.&#x20;

```xml
<DecimalPlaces Value="0" />
```

Необязательный тэг. Значение тэга не ожидается.&#x20;

Обязательный атрибут `Value` ожидает неотрицательное целочисленное значение. По умолчанию используется значение 0.

### ThousandsSeparator <a href="#column_thousands_separator" id="column_thousands_separator"></a>

Признак, показывающий, отображается ли разделитель групп разрядов.&#x20;

```xml
<ThousandsSeparator Value="False" />
```

Необязательный тэг. Значение тэга не ожидается.&#x20;

Обязательный атрибут `Value` ожидает логическое значение. По умолчанию используется значение False.
