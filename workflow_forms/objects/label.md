---
description: >-
  Графический объект; элемент пользовательского интерфейса, отображающий текст
  для пользователя.
---

# Label

## Шаблон Label <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="" Type="Label" Assembly="BaseControls" ChangeForm="">
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
  <!--Тэги, специфичные для Label-->
  <Blink></Blink>
  <BlinkInterval></BlinkInterval>
  <TextAlign></TextAlign>
  <AutoSize></AutoSize>
  <DisableCopyingByDoubleClick></DisableCopyingByDoubleClick>
  <Text></Text>
</MyObject>
```

## Описание Label <a href="#description" id="description"></a>

```xml
<MyObject Name="LabelName" Type="Label" Assembly="BaseControls">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для Label-->
</MyObject>
```

### Получение значения <a href="#get-value" id="get-value"></a>

Значением `Label` считается текст надписи.

```xml
<Object Name="LabelName" />
```

### Задание значения <a href="#set-value" id="set-value"></a>

Любое значение будет переведено в текстовое.

```xml
<Object Name="LabelName"></Object>
```

## Тэги, специфичные для Label <a href="#specific-tags" id="specific-tags"></a>

### Blink <a href="#blink" id="blink"></a>

Признак мерцания надписи.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<Blink>False</Blink>
```

### BlinkInterval <a href="#blink_interval" id="blink_interval"></a>

Интервал мерцания надписи (в миллисекундах).

Необязательный тэг. Ожидается целочисленное значение.

По умолчанию используется значение 500.

```xml
<BlinkInterval>500</BlinkInterval>
```

### TextAlign <a href="#text_align" id="text_align"></a>

Название типа положения текста надписи.

Необязательный тэг. Ожидается название одного из типов положения текста:

<table data-header-hidden><thead><tr><th width="214" align="center"></th><th width="437.3333333333333"></th></tr></thead><tbody><tr><td align="center">TopLeft</td><td>Слева сверху</td></tr><tr><td align="center">TopCenter</td><td>По центру сверху</td></tr><tr><td align="center">TopRight</td><td>Справа сверху</td></tr><tr><td align="center">MiddleLeft</td><td>Слева посередине</td></tr><tr><td align="center">MiddleCenter</td><td>По центру посередине</td></tr><tr><td align="center">MiddleRight</td><td>Справа посередине</td></tr><tr><td align="center">BottomLeft</td><td>Слева снизу</td></tr><tr><td align="center">BottomCenter</td><td>По центру снизу</td></tr><tr><td align="center">BottomRight</td><td>Справа снизу</td></tr></tbody></table>

Если тэг `<TextAlign>` отсутствует, то используется значение MiddleLeft.

```xml
<TextAlign>MiddleLeft</TextAlign>
```

### Text <a href="#text" id="text"></a>

Текст надписи.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Text>Текст</Text>
```

### AutoSize <a href="#auto_size" id="auto_size"></a>

Признак, определяющий, будет ли ширина автоматически подстраиваться под содержание.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<AutoSize>True</AutoSize>
```

### DisableCopyingByDoubleClick <a href="#disable_copying_by_double_click" id="disable_copying_by_double_click"></a>

Признак, отключающий возможность копировать текст надписи по двойному клику.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<DisableCopyingByDoubleClick>True</DisableCopyingByDoubleClick>
```

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### Blink <a href="#get_blink" id="get_blink"></a>

Возвращает признак мерцания надписи.

```xml
<Object Name="LabelName">
  <Property Name="Blink" />
</Object>
```

### BlinkInterval <a href="#get_blink_interval" id="get_blink_interval"></a>

Возвращает интервал мерцания надписи (в миллисекундах).

```xml
<Object Name="LabelName">
  <Property Name="BlinkInterval" />
</Object>
```

### TextAlign <a href="#get_text_align" id="get_text_align"></a>

Возвращает название типа положения текста надписи.

```xml
<Object Name="LabelName">
  <Property Name="TextAlign" />
</Object>
```

### Text <a href="#get_text" id="get_text"></a>

Возвращает текст надписи.

```xml
<Object Name="LabelName">
  <Property Name="Text" />
</Object>
```

## Set-проперти для динамического задания свойств <a href="#get-properties" id="get-properties"></a>

### Blink <a href="#set_blink" id="set_blink"></a>

Задает признак мерцания надписи.

Ожидается логическое значение.

```xml
<Object Name="LabelName">
  <Property Name="Blink">True</Property>
</Object>
```

### BlinkInterval <a href="#set_blink_interval" id="set_blink_interval"></a>

Задает интервал мерцания надписи (в миллисекундах).

Ожидается целочисленное значение.

```xml
<Object Name="LabelName">
  <Property Name="BlinkInterval">1000</Property>
</Object>
```

### TextAlign <a href="#set_text_align" id="set_text_align"></a>

Задает название типа положения текста надписи.

Ожидается одно из названий типов положения текста.

```xml
<Object Name="LabelName">
  <Property Name="TextAlign">TopLeft</Property>
</Object>
```

### Text <a href="#set_text" id="set_text"></a>

Задает текст надписи.

Любое значение будет переведено в текстовое.

```xml
<Object Name="LabelName">
  <Property Name="Text">Text</Property>
</Object>
```
