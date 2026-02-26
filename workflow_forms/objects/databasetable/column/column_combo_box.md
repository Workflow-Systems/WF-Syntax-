---
description: >-
  Позволяет пользователям выбирать значение из выпадающего списка, если в
  таблице разрешено редактирование
---

# ColumnComboBox

## Шаблон DatabaseTableColumnComboBox <a href="#template_databasetable" id="template_databasetable"></a>

Перечень всех возможных тэгов столбца:

```xml
<Column Name="" Type="DatabaseTableColumnComboBox" Assembly="DatabaseTableColumnControls" >
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
  <!--Тэги, специфичные для DatabaseTableColumnComboBox-->
  <Sorted Value="" />
  <ValueList></ValueList>
</Column>
```

{% hint style="info" %}
Тэги, общие для всех типов столбцов описаны в статье [Column](./).
{% endhint %}

## Тэги, специфичные для столбцов типа DatabaseTableColumnComboBox <a href="#column_combo_box_tags" id="column_combo_box_tags"></a>

### Sorted <a href="#column_sorted" id="column_sorted"></a>

Признак, определяющий, будут ли элементы в выпадающем списке столбца ComboBox отсортированы по отображаемому значению.

```xml
<Sorted Value="False" />
```

Необязательный тэг. Значение тэга не ожидается.

Обязательный атрибут `Value` ожидает логическое значение. По умолчанию используется значение False.

### ValueList <a href="#column_value_list" id="column_value_list"></a>

Элементы выпадающего списка столбца.

```xml
<ValueList>
  <DataConnection SourceDataConnection="SourceDataConnectionName">
    <Fields>
      <Field Name="Field1Name" />
      <Field Name="Field2Name" />
    </Fields>
  </DataConnection>
</ValueList>
```

Обязательный тэг. Ожидается таблица с двумя столбцами. Первый столбец должен содержать реальные значения элементов, а второй - их отображаемое значение.
