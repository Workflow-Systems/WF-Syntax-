---
description: Используется для отображения столбцов логических данных в виде CheckBox
---

# ColumnCheckBox

## Шаблон DatabaseTableColumnCheckBox <a href="#template_databasetable" id="template_databasetable"></a>

Перечень всех возможных тэгов столбца:

```xml
<Column Name="" Type="DatabaseTableColumnCheckBox" Assembly="DatabaseTableColumnControls" >
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
  <!--Тэги, специфичные для DatabaseTableColumnCheckBox-->
  <ThreeState Value="" />
  <HeaderCheckAll Value="" />
</Column>
```

{% hint style="info" %}
Тэги, общие для всех типов столбцов описаны в статье [Column](./).
{% endhint %}

## Тэги, специфичные для столбцов типа DatabaseTableColumnCheckBox <a href="#column_combo_box_tags" id="column_combo_box_tags"></a>

### ThreeState <a href="#column_three_state" id="column_three_state"></a>

Признак, определяющий, будут ли ячейки столбца CheckBox иметь промежуточное состояние.

```xml
<ThreeState Value="False" />
```

Необязательный тэг. Значение тэга не ожидается.&#x20;

Обязательный атрибут `Value` ожидает логическое значение. По умолчанию используется значение False.

### HeaderCheckAll <a href="#column_header_check_all" id="column_header_check_all"></a>

Признак, определяющий, будет ли заголовок столбца содержать галочку, которая управляет всеми значениями столбца одновременно.

```xml
<HeaderCheckAll Value="False" />
```

Необязательный тэг. Значение тэга не ожидается.&#x20;

Обязательный атрибут `Value` ожидает логическое значение. По умолчанию используется значение False.
