---
description: Фильтр полученных данных.
---

# Filter

Используется в [PrimaryGetDataConnection](./), [SecondaryGetDataConnection](../secondary_dc.md), [ConvertDataConnection](../convert_dc/) и [TreeGetDataConnection](../tree_get_dc.md).

## Шаблон Filter <a href="#filter" id="filter"></a>

#### Вариант одиночного фильтра

```xml
<Filter Type="Equal" FilterByNullValue="" RefreshFilter="" Reverse="">
  <Field NativeName="" />
  <Value></Value>
  <DataType Type="" />
  <Enabled></Enabled>
</Filter>
```

#### Вариант фильтра-выражения

```xml
<Filter Type="Nested" FilterByNullValue="">
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

## Описание Filter <a href="#filter" id="filter"></a>

Одиночный фильтр:

```xml
<Filter Type="" FilterByNullValue="" RefreshFilter="" Reverse="">
  <!--Тэги, специфичные для Filter-->
</Filter>
```

Фильтр-выражение:

```xml
<Filter Type="Nested" FilterByNullValue="True">
  <!--Тэги <And>, <Or> и <Not>-->
</Filter>
```

Необязательный атрибут `Type` - тип сравнения значений.\
Ожидается название одного из [типов сравнения](filter.md#filter_types) значений. По умолчанию используется значение Equal. Атрибуту можно задать значение Nested, чтобы сделать фильтр-выражение.

Необязательный атрибут `FilterByNullValue` - признак, определяющий, будет ли осуществляться фильтрация для очередной строки соединения с данными, если значение фильтра будет равно NULL.\
Ожидается логическое значение. По умолчанию используется значение True.

Необязательный атрибут `RefreshFilter` - признак, определяющий, будут ли данные сразу же отфильтрованы при изменении параметра фильтра.\
Ожидается логическое значение. По умолчанию используется значение True.

Необязательный атрибут `Reverse` - признак, определяющий, будет ли изменён порядок аргументов фильтра на обратный.\
Ожидается логическое значение. По умолчанию используется значение False.

{% hint style="warning" %}
Атрибуты `RefreshFilter` и `Reverse` не работают для фильтров-выражений (атрибут `Type` со значением Nested).\
Для таких фильтров данные обновляются всегда.
{% endhint %}

## Тэги, специфичные для Filter  <a href="#option_1_tags_primary_dc" id="option_1_tags_primary_dc"></a>

{% hint style="warning" %}
Перечисленные ниже тэги не допустимы для фильтров-выражений (атрибут `Type` со значением Nested).
{% endhint %}

### Field <a href="#filter_field" id="filter_field"></a>

Поле, по значению которого полученные данные фильтруются.

```xml
<Field NativeName="FieldName" />
```

Обязательный тэг. Значение не ожидается.

Обязательный атрибут `NativeName` - название поля, по значению которого полученные данные фильтруются. Ожидается название одного из полей, описанных в тэге `<Fields>`.

### Value <a href="#filter_value" id="filter_value"></a>

Значение, по которому полученные данные фильтруются.

```xml
<Value>Value</Value>
```

Обязательный тэг. Ожидается любое значение.

### DataType <a href="#filter_data_type" id="filter_data_type"></a>

Тип данных, к которому приводятся сравниваемые значения.

```xml
<DataType Type="DataTypeName" Precision="Integer"/>
```

Необязательный тэг. Значение не ожидается.

Обязательный атрибут `Type` - название типа данных. Ожидается название одного из типов данных, поддерживаемых формой. Полный список типов данных описан по [ссылке](../../data_types/).

Если тэг `<DataType>` отсутствует, то для атрибута `Type` используется значение StringDataType.

Необязательный атрибут `Precision` - задает точность сравнения чисел. Ожидается неотрицательное целое значение. По умолчанию используется значение 2.

### Enabled <a href="#filter_enabled" id="filter_enabled"></a>

Признак, определяющий, будет ли использоваться данный фильтр.

```xml
<Enabled>True</Enabled>
```

Необязательный тэг. Ожидается логическое значение.

## Типы сравнения значений <a href="#filter_types" id="filter_types"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="459.3333333333333"></th></tr></thead><tbody><tr><td align="center">Equal</td><td>Сравнение значений на равенство</td></tr><tr><td align="center">NotEqual</td><td>Сравнение значений на неравенство</td></tr><tr><td align="center">Greater</td><td>Сравнение значений на "больше": значение из соединения с данными больше указанного значения</td></tr><tr><td align="center">NotGreater</td><td>Сравнение значений на "не больше": значение из соединения с данными не больше указанного значения</td></tr><tr><td align="center">Less</td><td>Сравнение значений на "меньше": значение из соединения с данными меньше указанного значения</td></tr><tr><td align="center">NotLess</td><td>Сравнение значений на "не меньше": значение из соединения с данными не меньше указанного значения</td></tr><tr><td align="center">Contains</td><td>Сравнение значений на "содержит": значение из соединения с данными содержит указанное значение (значения любых типов данных преобразуются к строковому типу)</td></tr><tr><td align="center">NotContains</td><td>Сравнение значений на "не содержит": значение из соединения с данными не содержит указанное значение (значения любых типов данных преобразуются к строковому типу)</td></tr><tr><td align="center">In</td><td>Сравнение значений на "входит": значение из соединения с данными входит в указанный массив</td></tr><tr><td align="center">NotIn</td><td>Сравнение значений на "не входит": значение из соединения с данными не входит в указанный массив</td></tr><tr><td align="center">Overlap</td><td>Сравнение значений на "пересекается": массив из соединения с данными имеет общие элементы с указанным массивом</td></tr><tr><td align="center">NotOverlap</td><td>Сравнение значений на "не пересекается": массив из соединения с данными не имеет общих элементов с указанным массивом</td></tr><tr><td align="center">MatchSearch</td><td>Сравнение значений на "удовлетворяет поисковой строке": поисковая строка может состоять из слов, разделенных пробелами и знаками "+", "*" и "?"<em>,</em> пробел означает "ИЛИ", "+" означает "И", "*" означает любое количество любых символов, "?" означат ровно один символ</td></tr><tr><td align="center">NotMatchSearch</td><td>Сравнение значений на "не удовлетворяет поисковой строке": поисковая строка может состоять из слов, разделенных пробелами и знаками "+", "*" и "?"<em>,</em> пробел означает "ИЛИ", "+" означает "И", "*" означает любое количество любых символов, "?" означат ровно один символ</td></tr><tr><td align="center">ContainedIn</td><td>Сравнение значений на "входит": значение из соединения с данными входит в указанное значение (значения любых типов данных преобразуются к строковому типу)</td></tr><tr><td align="center">NotContainedIn</td><td>Сравнение значений на "не входит": значение из соединения с данными не входит в указанное значение (значения любых типов данных преобразуются к строковому типу)</td></tr></tbody></table>

## Логические операторы

{% hint style="warning" %}
Логические операторы допустимы только для фильтров-выражений (атрибут `Type` со значением Nested).
{% endhint %}

### And <a href="#filter_and" id="filter_and"></a>

Логическое умножение нескольких фильтров. Возвращает true, если все операнды одновременно равны true.

```xml
<And RefreshFilter="True" RefreshData="True">
  <Filter>
    <Field NativeName="" />
    <Value></Value>
    <DataType Type="" />
    <Enabled></Enabled>
  </Filter>
  <Not>
    <Filter>
      <Field NativeName="" />
      <Value></Value>
      <DataType Type="" />
      <Enabled></Enabled>
    </Filter>
  </Not>
</And>
```

Необязательный тэг. Ожидается список тэгов `<Filter>`, `<And>`, `<Or>` и `<Not>`.

Необязательный атрибут `RefreshFilter` - признак, определяющий, будут ли данные сразу же отфильтрованы при изменении вложенного фильтра.\
Ожидается логическое значение. По умолчанию используется значение True.

Необязательный атрибут `RefreshData` - признак, определяющий, будут ли данные обновлены из исходного соединения с данными перед фильтрацией. \
Ожидается логическое значение. По умолчанию используется значение False.

### Or <a href="#filter_or" id="filter_or"></a>

Логическое сложение нескольких фильтров. Возвращает true, если хотя бы один из операндов возвращает true.

```xml
<Or RefreshFilter="True" RefreshData="True">
  <Filter>
    <Field NativeName="" />
    <Value></Value>
    <DataType Type="" />
    <Enabled></Enabled>
  </Filter>
  <Filter>
    <Field NativeName="" />
    <Value></Value>
    <Enabled></Enabled>
  </Filter>
</Or>
```

Необязательный тэг. Ожидается список тэгов `<Filter>`, `<And>`, `<Or>` и `<Not>`.

Необязательный атрибут `RefreshFilter` - признак, определяющий, будут ли данные сразу же отфильтрованы при изменении вложенного фильтра.\
Ожидается логическое значение. По умолчанию используется значение True.

Необязательный атрибут `RefreshData` - признак, определяющий, будут ли данные обновлены из исходного соединения с данными перед фильтрацией. \
Ожидается логическое значение. По умолчанию используется значение False.

### Not <a href="#filter_not" id="filter_not"></a>

Логическое отрицание одного фильтра. Производится над одним операндом и возвращает true, если операнд равен false. Если операнд равен true, то операция возвращает false.

```xml
<Not RefreshFilter="True" RefreshData="True">
  <Filter>
    <Field NativeName="" />
    <Value></Value>
    <DataType Type="ypeName" />
    <Enabled></Enabled>
  </Filter>
</Not>
```

Необязательный тэг. Ожидается один из тэгов `<Filter>`, `<And>`, `<Or>` или `<Not>`.

Необязательный атрибут `RefreshFilter` - признак, определяющий, будут ли данные сразу же отфильтрованы при изменении значения вложенного фильтра.\
Ожидается логическое значение. По умолчанию используется значение True.

Необязательный атрибут `RefreshData` - признак, определяющий, будут ли данные обновлены из исходного соединения с данными перед фильтрацией. \
Ожидается логическое значение. По умолчанию используется значение False.
