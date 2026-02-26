---
description: >-
  Графический объект. Группа переключателей. Включение одного переключателя
  означает отключение всех остальных.
---

# RadioButtonBlock

## Шаблон RadioButtonBlock <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="" Type="RadioButtonBlock" Assembly="BaseControls" ChangeForm="">
  <!--Тэги, общие для всех графических объектов-->
  <Top></Top>
  <Bottom></Bottom>
  <Left></Left>
  <Right></Right>
  <Height></Height>
  <Width></Width>
  <FontStyle></FontStyle>
  <ForeColor></ForeColor>
  <BackColor></BackColor>
  <Enabled></Enabled>
  <Visible></Visible>
  <Hint></Hint>
  <ContextMenu Name="" />
  <Change User="" Source="" ValueSet="" />
  <!--Тэги, специфичные для RadioButtonBlock-->
  <Appearance></Appearance>
  <FlatCheckedBackColor></FlatCheckedBackColor>
  <Options>
    <Option Name="">
      <Top></Top>
      <Left></Left>
      <Height></Height>
      <Width></Width>
      <FontStyle></FontStyle>
      <ForeColor></ForeColor>
      <BackColor></BackColor>
      <Enabled></Enabled>
      <Visible></Visible>
      <Hint></Hint>
      <ContextMenu Name="" />
      <Change User="" Source="" ValueSet="" />
      <Text></Text>
      <Checked></Checked>
      <Value></Value>
    </Option>
  </Options>
  <Value></Value>
</MyObject>
```

## Описание RadioButtonBlock <a href="#description" id="description"></a>

```xml
<MyObject Name="RadioButtonBlockName" Type="RadioButtonBlock" Assembly="BaseControls">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для RadioButtonBlock-->
</MyObject>
```

### Получение значения <a href="#get-value" id="get-value"></a>

Значением RadioButtonBlock считается значение активного переключателя.

Для получения значения используется get-проперти [Value](./#get_value):

```xml
<Object Name="RadioButtonBlockName">
  <Property Name="Value" />
</Object>
```

Рекомендуется использовать сокращенный вариант записи:

```xml
<Object Name="RadioButtonBlockName" />
```

### Задание значения <a href="#set-value" id="set-value"></a>

Для задания значения используется set-проперти [Value](./#set_value):

```xml
<Object Name="RadioButtonBlockName">
  <Property Name="Value">Текст</Property>
</Object>
```

Рекомендуется использовать сокращенный вариант записи:

```xml
<Object Name="RadioButtonBlockName">Текст</Object>
```

## Тэги, специфичные для RadioButtonBlock <a href="#specific-tags" id="specific-tags"></a>

### Options <a href="#options" id="options"></a>

Содержит список переключателей.

Необязательный тэг. Ожидает список тэгов [`<Option>`](option.md), содержащих описание переключателей.

```xml
<Options></Options>
```

### Value <a href="#value" id="value"></a>

Задает значение, определяющее активный переключатель.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Value>Value</Value>
```

### Appearance

Задает значение, определяющее внешний вид переключателей.

Необязательный тэг. Ожидается одно из допустимых значений:

<table data-header-hidden><thead><tr><th width="234.41687935952444" align="center"></th><th width="415.40287769784175"></th></tr></thead><tbody><tr><td align="center">Normal</td><td>Переключатели отображаются в виде круглых флажков</td></tr><tr><td align="center">Button</td><td>Переключатели отображаются в виде плоских кнопок</td></tr></tbody></table>

По умолчанию используется значение Normal.

```xml
<Appearance>Button</Appearance>
```

### FlatCheckedBackColor <a href="#flat_checked_back_color" id="flat_checked_back_color"></a>

Задает цвет активного переключателя.

Необязательный тег. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется 20-и %-ый серый цвет.

```xml
<FlatCheckedBackColor>LightGreen</FlatCheckedBackColor>
```

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### Value <a href="#get_value" id="get_value"></a>

Возвращает значение, определяющее активный переключатель.

```xml
<Object Name="RadioButtonBlockName">
  <Property Name="Value" />
</Object>
```

### Text <a href="#get_text" id="get_text"></a>

Возвращает текст активного переключателя или переключателя, название которого задано в параметре.

Значение тэга `<Property>`: тэг `<Parameters>` со вложенными тэгами `<Parameter>`, один из которых имеет атрибут `Name`, равный Option.

```xml
<Object Name="RadioButtonBlockName">
  <Property Name="Text">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным Option: ожидается название одной из радиокнопок-->
      <Parameter Name="Option">OptionName</Parameter>
    </Parameters>
  </Property>
</Object>
```

Если значение тэга `<Property>` отсутствует, то будет возвращен текст активного переключателя.

```xml
<Object Name="RadioButtonBlockName">
  <Property Name="Text" />
</Object>
```

### Checked <a href="#get_checked" id="get_checked"></a>

Возвращает признак выбора переключателя [`<Option>`](option.md) из группы.

```xml
<Object Name="RadioButtonBlockName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter, один из которых имеет атрибут Name, равный Option-->
  <Property Name="Checked">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным Option: ожидается название одного из переключателей-->
      <Parameter Name="Option">OptionName</Parameter>
    </Parameters>
  </Property>
</Object>
```

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

### Value <a href="#set_value" id="set_value"></a>

Задает значение, определяющее активный переключатель.

```xml
<Object Name="RadioButtonBlockName">
  <Property Name="Value">Text</Property>
</Object>
```

### Text <a href="#set_text" id="set_text"></a>

Задает текст активного переключателя или переключателя, название которого задано в параметре.

```xml
<Object Name="RadioButtonBlockName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="Text">
    <Parameters>
      <!--Необязательный параметр. При отсутствии обновляет текст активного переключателя-->
      <!--Значение тэга Parameter с атрибутом Name, равным Option: ожидается название одного из переключателей-->
      <Parameter Name="Option">OptionName</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным Value: любое значение будет переведено в текстовое-->
      <Parameter Name="Value">Text</Parameter>
    </Parameters>
  </Property>
</Object>
```

### Checked <a href="#set_checked" id="set_checked"></a>

Задает признак выбора переключателя [`<Option>`](option.md) из группы.

```xml
<Object Name="RadioButtonBlockName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="Checked">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным Option: ожидается название одного из переключателей-->
      <Parameter Name="Option">OptionName</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным Value: ожидается логическое значение-->
      <Parameter Name="Value">True</Parameter>
    </Parameters>
  </Property>
</Object>
```
