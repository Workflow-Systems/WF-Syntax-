---
description: >-
  Используется для отображения дат и времени в заданном формате и предоставляет
  пользователю возможностью выбирать значение в раскрывающемся календаре, если в
  таблице разрешено редактирование
---

# ColumnDateTimePicker

## Шаблон DatabaseTableColumnDateTimePicker <a href="#template_databasetable" id="template_databasetable"></a>

Перечень всех возможных тэгов столбца:

```xml
<Column Name="" Type="DatabaseTableColumnDateTimePicker" Assembly="DatabaseTableColumnControls" >
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
  <!--Тэги, специфичные для DatabaseTableColumnDateTimePicker-->
  <Format Value="" />
  <NullValue Show="" />
  <ShowCalendar Value="" />
</Column>
```

{% hint style="info" %}
Тэги, общие для всех типов столбцов описаны в статье [Column](./).
{% endhint %}

## Тэги, специфичные для столбцов типа DatabaseTableColumnDateTimePicker <a href="#column_combo_box_tags" id="column_combo_box_tags"></a>

### Format <a href="#column_format" id="column_format"></a>

Формат даты в ячейках столбца.

```xml
<Format Value="dd MM yyyy" />
```

Необязательный тэг. Значение тэга не ожидается.&#x20;

Обязательный атрибут `Value` ожидает строку формата даты/времени. По умолчанию используется значение "dd MM yyyy".

### NullValue <a href="#column_null_value" id="column_null_value"></a>

Признак, определяющий, может ли дата иметь значение NULL.

```xml
<NullValue Show="True" />
```

Необязательный тэг. Значение тэга не ожидается.&#x20;

Обязательный атрибут `Show` ожидает логическое значение. По умолчанию используется значение True.

### ShowCalendar <a href="#column_show_calendar" id="column_show_calendar"></a>

Признак, определяющий, будет ли показываться календарь.

```xml
<ShowCalendar Value="True" />
```

Необязательный тэг. Значение тэга не ожидается.&#x20;

Обязательный атрибут `Value` ожидает логическое значение. По умолчанию используется значение True.
