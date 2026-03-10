---
description: Графический объект; поле для выбора числа.
---

# NumericBox

## Шаблон NumericBox <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="" Type="NumericBox" Assembly="BaseControls" ChangeForm="">
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
  <!--Тэги, специфичные для NumericBox-->
  <ReadOnly></ReadOnly>
  <SelectOnEnter></SelectOnEnter>
  <ScrollWithWheel></ScrollWithWheel>
  <Increment></Increment>
  <Maximum></Maximum>
  <Minimum></Minimum>
  <DecimalPlaces></DecimalPlaces>
  <ThousandsSeparator></ThousandsSeparator>
  <Value></Value>
</MyObject>
```

## Описание NumericBox <a href="#description" id="description"></a>

```xml
<MyObject Name="NumericBoxName" Type="NumericBox" Assembly="BaseControls">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для NumericBox-->
</MyObject>
```

### Получение значения <a href="#get-value" id="get-value"></a>

Значением NumericBox считается значение числа, указанного в поле.

```xml
<Object Name="NumericBoxName" />
```

### Задание значения <a href="#set-value" id="set-value"></a>

Ожидается числовое значение.

```xml
<Object Name="NumericBoxName"></Object>
```

## Тэги, специфичные для NumericBox <a href="#specific-tags" id="specific-tags"></a>

### ReadOnly <a href="#read_only" id="read_only"></a>

Признак, определяющий, запрещен ли ввод текста в поле для пользователя.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<ReadOnly>False</ReadOnly>
```

### ReadOnlyColor <a href="#read_only_color" id="read_only_color"></a>

Задает цвет фона объекта, если признак [ReadOnly](numericbox.md#read_only) имеет значение True.

Необязательный тэг. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется стандартное значение .NET.

```xml
<ReadOnlyColor>#607D8B</ReadOnlyColor>
```

### SelectOnEnter <a href="#select_on_enter" id="select_on_enter"></a>

Признак, определяющий, будет ли выделено содержимое поля после получения им фокуса.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<SelectOnEnter>False</SelectOnEnter>
```

### ScrollWithWheel <a href="#scroll_with_wheel" id="scroll_with_wheel"></a>

Признак, включающий или отключающий возможность изменять значение колесиком мышки.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение True.

```xml
<ScrollWithWheel>False</ScrollWithWheel>
```

### Increment <a href="#increment" id="increment"></a>

Число, на которое будет изменяться значение поля.

Необязательный тэг. Ожидается числовое значение.

По умолчанию используется значение 1.

```xml
<Increment>1</Increment>
```

### Maximum <a href="#maximum" id="maximum"></a>

Максимально допустимое число для ввода.

Необязательный тэг. Ожидается числовое значение.

Если тэг `<Maximum>` отсутствует, то ограничение на максимум не устанавливается.

```xml
<Maximum>100</Maximum>
```

### Minimum <a href="#minimum" id="minimum"></a>

Минимальное допустимое число для ввода.

Необязательный тэг. Ожидается числовое значение.

Если тэг `<Minimum>` отсутствует, то ограничение на минимум не устанавливается.

```xml
<Minimum>0</Minimum>
```

### DecimalPlaces <a href="#decimal_places" id="decimal_places"></a>

Количество знаков дробной части числа.

Необязательный тэг. Ожидается целочисленное значение.

По умолчанию используется значение 0.

```xml
<DecimalPlaces>0</DecimalPlaces>
```

### ThousandsSeparator <a href="#thousands_separator" id="thousands_separator"></a>

Признак, показывающий, отображается ли разделитель групп разрядов.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<ThousandsSeparator>False</ThousandsSeparator>
```

### Value <a href="#value" id="value"></a>

Число в поле.

Необязательный тэг. Ожидается числовое значение.

По умолчанию используется значение NULL.

```xml
<Value>1</Value>
```

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### ReadOnly <a href="#get_read_only" id="get_read_only"></a>

Возвращает признак, определяющий, запрещен ли ввод текста в поле для пользователя.

```xml
<Object Name="NumericBoxName">
  <Property Name="ReadOnly" />
</Object>
```

### SelectOnEnter <a href="#get_select_on_enter" id="get_select_on_enter"></a>

Возвращает признак, определяющий, будет ли выделено содержимое поля после получения им фокуса.

```xml
<Object Name="NumericBoxName">
  <Property Name="SelectOnEnter" />
</Object>
```

### Increment <a href="#get_increment" id="get_increment"></a>

Возвращает число, на которое будет изменяться значение поля.

```xml
<Object Name="NumericBoxName">
  <Property Name="Increment" />
</Object>
```

### Maximum <a href="#get_maximum" id="get_maximum"></a>

Возвращает максимально допустимое число для ввода.

```xml
<Object Name="NumericBoxName">
  <Property Name="Maximum" />
</Object>
```

### Minimum <a href="#get_minimum" id="get_minimum"></a>

Возвращает минимальное допустимое число для ввода.

```xml
<Object Name="NumericBoxName">
  <Property Name="Minimum" />
</Object>
```

### DecimalPlaces <a href="#get_decimal_places" id="get_decimal_places"></a>

Возвращает количество знаков дробной части числа.

```xml
<Object Name="NumericBoxName">
  <Property Name="DecimalPlaces" />
</Object>
```

### ThousandsSeparator <a href="#get_thousands_separator" id="get_thousands_separator"></a>

Возвращает признак, показывающий, отображается ли разделитель групп разрядов.

```xml
<Object Name="NumericBoxName">
  <Property Name="ThousandsSeparator" />
</Object>
```

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

### ReadOnly <a href="#set_read_only" id="set_read_only"></a>

Задает признак, определяющий, запрещен ли ввод текста в поле для пользователя.

Ожидается логическое значение.

```xml
<Object Name="NumericBoxName">
  <Property Name="ReadOnly">True</Property>
</Object>
```

### SelectOnEnter <a href="#set_select_on_enter" id="set_select_on_enter"></a>

Задает признак, определяющий, будет ли выделено содержимое поля после получения им фокуса.

Ожидается логическое значение.

```xml
<Object Name="NumericBoxName">
  <Property Name="SelectOnEnter">True</Property>
</Object>
```

### Increment <a href="#set_increment" id="set_increment"></a>

Задает число, на которое будет изменяться значение поля.

Ожидается числовое значение.

```xml
<Object Name="NumericBoxName">
  <Property Name="Increment">0,1</Property>
</Object>
```

### Maximum <a href="#set_maximum" id="set_maximum"></a>

Задает максимально допустимое число для ввода.

Ожидается числовое значение.

```xml
<Object Name="NumericBoxName">
  <Property Name="Maximum">1000</Property>
</Object>
```

### Minimum <a href="#set_minimum" id="set_minimum"></a>

Задает минимальное допустимое число для ввода.

Ожидается числовое значение.

```xml
<Object Name="NumericBoxName">
  <Property Name="Minimum">-1000</Property>
</Object>
```

### DecimalPlaces <a href="#set_decimal_places" id="set_decimal_places"></a>

Задает количество знаков дробной части числа.

Ожидается целочисленное значение.

```xml
<Object Name="NumericBoxName">
  <Property Name="DecimalPlaces">3</Property>
</Object>
```

### ThousandsSeparator <a href="#set_thousands_separator" id="set_thousands_separator"></a>

Задает признак, показывающий, отображается ли разделитель групп разрядов.

Ожидается логическое значение.

```xml
/<Object Name="NumericBoxName">
  <Property Name="ThousandsSeparator">True</Property>
</Object>
```
