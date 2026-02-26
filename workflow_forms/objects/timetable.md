---
description: >-
  Графический объект; таблица, отображающая в строках интервалы времени для
  набора элементов за указанный период.
---

# TimeTable

## Шаблон TimeTable <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="" Type="TimeTable" Assembly="ComplexControls" ChangeForm="">
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
  <Change User="" Source="" ValueSet="" />
  <!--Тэги, специфичные для TimeTable-->
  <RowHeight Value="" />
  <ColumnHeadersHeight Value="" />
  <ColumnHeadersVisible Value="" />
  <RowHeadersWidth Value="" />
  <RowHeadersVisible Value="" />
  <BackgroundColor Value="" />
  <BorderStyle Value="" />
  <CellBorderStyle Value="" />
  <AutoSizeRowsMode Value="" />
  <ValueSeparator Value="" />
  <ColumnWidth Value="" />
  <ColumnAlignment Value="" />
  <ColumnHeaderAlignment Value="" />
  <DateStart></DateStart>
  <DateFinish></DateFinish>
  <Data>
    <DataConnection SourceDataConnection="DataPrimaryGetDataConnection">
      <SourceQuery Name="Items">
        <Fields>
          <Field Name="" />
          <Field Name="" />
        </Fields>
      </SourceQuery>
      <SourceQuery Name="Colors">
        <Fields>
          <Field Name="" />
          <Field Name="" />
          <Field Name="" />
          <Field Name="" />
        </Fields>
      </SourceQuery>
      <SourceQuery Name="Intervals">
        <Fields>
          <Field Name="" />
          <Field Name="" />
          <Field Name="" />
          <Field Name="" />
          <Field Name="" />
          <Field Name="" />
          <Field Name="" />
          <Field Name="" />
        </Fields>
      </SourceQuery>
    </DataConnection>
  </Data>
  <Interval Type="" Value="" TitleFormat="" />
  <MultiSelect></MultiSelect>
</MyObject>
```

## Описание TimeTable <a href="#description" id="description"></a>

```xml
<MyObject Name="TimeTableName" Type="TimeTable" Assembly="ComplexControls">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для TimeTable-->
</MyObject>
```

TimeTable не имеет значения.

## Тэги, специфичные для TimeTable <a href="#specific-tags" id="specific-tags"></a>

### RowHeight <a href="#row_height" id="row_height"></a>

Высота строк с данными в таблице.

Необязательный тэг. Значение тэга `<RowHeight>`: не ожидается.

Если тэг `<RowHeight>` отсутствует, то для атрибута `Value` используется стандартное значение .NET.

```xml
<RowHeight Value="22" />
```

#### Атрибуты тэга `<RowHeight>` <a href="#attributes_tag_row_height" id="attributes_tag_row_height"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="499.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается целочисленное значение.</p></td></tr></tbody></table>

### ColumnHeadersHeight <a href="#column_headers_height" id="column_headers_height"></a>

Высота "шапки" таблицы.

Необязательный тэг. Значение тэга `<ColumnHeadersHeight>`: не ожидается.

Если тэг `<ColumnHeadersHeight>` отсутствует, то для атрибута `Value` используется стандартное значение .NET.

```xml
<ColumnHeadersHeight Value="21" />
```

#### Атрибуты тэга `<ColumnHeadersHeight>` <a href="#attributes_tag_column_headers_height" id="attributes_tag_column_headers_height"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="499.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается целочисленное значение.</p></td></tr></tbody></table>

### ColumnHeadersVisible <a href="#column_headers_visible" id="column_headers_visible"></a>

Признак, определяющий, показывать или нет "шапку" таблицы.

Необязательный тэг. Значение тэга `<ColumnHeadersVisible>`: не ожидается.

Если тэг `<ColumnHeadersVisible>` отсутствует, то для атрибута `Value` используется значение True.

```xml
<ColumnHeadersVisible Value="True" />
```

#### Атрибуты тэга `<ColumnHeadersVisible>` <a href="#attributes_tag_column_headers_visible" id="attributes_tag_column_headers_visible"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="499.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

### RowHeadersWidth <a href="#row_headers_width" id="row_headers_width"></a>

Ширина "нулевого" столбца таблицы, где расположены названия элементов.

Необязательный тэг. Значение тэга `<RowHeadersWidth>`: не ожидается.

Если тэг `<RowHeadersWidth>` отсутствует, то для атрибута `Value` используется значение 100.

```xml
<RowHeadersWidth Value="40" />
```

#### Атрибуты тэга `<RowHeadersWidth>` <a href="#attributes_tag_row_headers_width" id="attributes_tag_row_headers_width"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="499.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается целочисленное значение.</p></td></tr></tbody></table>

### RowHeadersVisible <a href="#row_headers_visible" id="row_headers_visible"></a>

Признак, определяющий, показывать или нет "нулевой" столбец таблицы, где расположены названия элементов.

Необязательный тэг. Значение тэга `<RowHeadersVisible>`: не ожидается.

Если тэг `<RowHeadersVisible>` отсутствует, то для атрибута `Value` используется значение True.

```xml
<RowHeadersVisible Value="True" />
```

#### Атрибуты тэга `<RowHeadersVisible>` <a href="#attributes_tag_row_headers_visible" id="attributes_tag_row_headers_visible"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="499.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

### BackgroundColor <a href="#background_color" id="background_color"></a>

Цвет фона таблицы.

Необязательный тэг. Значение тэга `<BackgroundColor>`: не ожидается.

Если тэг `<BackgroundColor>` отсутствует, то для атрибута `Value` используется стандартное значение .NET.

```xml
<BackgroundColor Value="BackgroundColor" />
```

#### Атрибуты тэга `<BackgroundColor>` <a href="#attributes_tag_background_color" id="attributes_tag_background_color"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="499.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).</p></td></tr></tbody></table>

### BorderStyle <a href="#border_style" id="border_style"></a>

Название типа границ таблицы.

Необязательный тэг. Значение тэга `<BorderStyle>`: не ожидается.

Если тэг `<BorderStyle>` отсутствует, то для атрибута `Value` используется значение FixedSingle.

```xml
<BorderStyle Value="FixedSingle" />
```

#### Атрибуты тэга `<BorderStyle>` <a href="#attributes_tag_border_style" id="attributes_tag_border_style"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="499.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается название одного из <a href="timetable.md#border_style_types">типов границ</a> таблицы.</p></td></tr></tbody></table>

#### Типы границ таблицы <a href="#border_style_types" id="border_style_types"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="499.3333333333333"></th></tr></thead><tbody><tr><td align="center">None</td><td>Нет границ</td></tr><tr><td align="center">FixedSingle</td><td>Одиночная плоская</td></tr><tr><td align="center">Fixed3D</td><td>Одиночная объемная</td></tr></tbody></table>

### CellBorderStyle <a href="#cell_border_style" id="cell_border_style"></a>

Название стиля границ ячеек в таблице.

Необязательный тэг. Значение тэга `<CellBorderStyle>`: не ожидается.

Если тэг `<CellBorderStyle>` отсутствует, то для атрибута `Value` используется значение Single.

```xml
<CellBorderStyle Value="Single" />
```

#### Атрибуты тэга `<CellBorderStyle>` <a href="#attributes_tag_cell_border_style" id="attributes_tag_cell_border_style"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="499.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается название одного из <a href="timetable.md#cell_border_style_types">стилей границ</a> ячеек в таблице.</p></td></tr></tbody></table>

#### Стили границ ячеек <a href="#cell_border_style_types" id="cell_border_style_types"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="499.3333333333333"></th></tr></thead><tbody><tr><td align="center">Custom</td><td>Граница, которая была настроена</td></tr><tr><td align="center">Single</td><td>Одинарная граница</td></tr><tr><td align="center">Raised</td><td>Трехмерная выпуклая граница</td></tr><tr><td align="center">Sunken</td><td>Трехмерная утопленная граница</td></tr><tr><td align="center">None</td><td>Отсутствие границ</td></tr><tr><td align="center">SingleVertical</td><td>Вертикальная одинарная граница</td></tr><tr><td align="center">RaisedVertical</td><td>Вертикальная трехмерная выпуклая граница</td></tr><tr><td align="center">SunkenVertical</td><td>Вертикальная трехмерная утопленная граница</td></tr><tr><td align="center">SingleHorizontal</td><td>Горизонтальная одинарная граница</td></tr><tr><td align="center">RaisedHorizontal</td><td>Горизонтальная трехмерная выпуклая граница</td></tr><tr><td align="center">SunkenHorizontal</td><td>Горизонтальная трехмерная утопленная граница</td></tr></tbody></table>

### AutoSizeRowsMode <a href="#auto_size_rows_mode" id="auto_size_rows_mode"></a>

Название типа автоматического изменения высоты строк таблицы.

Необязательный тэг. Значение тэга `<AutoSizeRowsMode>`: не ожидается.

Если тэг `<AutoSizeRowsMode>` отсутствует, то для атрибута `Value` используется значение None.

```xml
<AutoSizeRowsMode Value="None" />
```

#### Атрибуты тэга `<AutoSizeRowsMode>` <a href="#attributes_tag_auto_size_rows_mode" id="attributes_tag_auto_size_rows_mode"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="499.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается название одного из <a href="timetable.md#auto_size_rows_mode_types">типов автоматического изменения высоты</a> строк таблицы.</p></td></tr></tbody></table>

#### Типы автоматического изменения высоты строк таблицы <a href="#auto_size_rows_mode_types" id="auto_size_rows_mode_types"></a>

<table data-header-hidden><thead><tr><th width="287.1847118442168" align="center"></th><th width="456.05119872487694"></th></tr></thead><tbody><tr><td align="center">None</td><td>Нет автоматического изменения высоты строк таблицы</td></tr><tr><td align="center">AllCells</td><td>Высота строк изменяется в соответствии с содержимым всех ячеек в строках, включая ячейки заголовка</td></tr><tr><td align="center">AllCellsExceptHeaders</td><td>Высота строк изменяется в соответствии с содержимым всех ячеек в строках, исключая ячейки заголовка</td></tr><tr><td align="center">AllHeaders</td><td>Высота строк изменяется в соответствии с содержимым заголовка строк</td></tr><tr><td align="center">DisplayedCells</td><td>Высота строк изменяется в соответствии с содержимым всех ячеек в строках, отображаемых в текущий момент на экране, включая ячейки заголовка</td></tr><tr><td align="center">DisplayedCellsExceptHeaders</td><td>Высота строк изменяется в соответствии с содержимым всех ячеек в строках, отображаемых в текущий момент на экране, исключая ячейки заголовка</td></tr><tr><td align="center">DisplayedHeaders</td><td>Высота строк изменяется в соответствии с содержимым заголовков строк, отображаемых в текущий момент на экране</td></tr></tbody></table>

### ValueSeparator <a href="#value_separator" id="value_separator"></a>

Текстовый разделитель для нескольких значений в одной ячейке таблицы.

Необязательный тэг. Значение тэга `<ValueSeparator>`: не ожидается.

Если тэг `<ValueSeparator>` отсутствует, то для атрибута `Value` используется значение " ".

Поддерживается символ "\r", который интерпретируется как перенос на новую строку.

```xml
<ValueSeparator Value="\r" />
```

#### Атрибуты тэга `<ValueSeparator>` <a href="#attributes_tag_value_separator" id="attributes_tag_value_separator"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="499.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Любое значение будет переведено в текстовое.</p></td></tr></tbody></table>

### ColumnWidth <a href="#column_width" id="column_width"></a>

Ширина столбцов таблицы.

Необязательный тэг. Значение тэга `<ColumnWidth>`: не ожидается.

Если тэг `<ColumnWidth>` отсутствует, то для атрибута `Value` используется значение 50.

```xml
<ColumnWidth Value="50" />
```

#### Атрибуты тэга `<ColumnWidth>` <a href="#attributes_tag_column_width" id="attributes_tag_column_width"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="499.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается положительное целочисленное значение.</p></td></tr></tbody></table>

### ColumnAlignment <a href="#column_alignment" id="column_alignment"></a>

Название типа положения содержимого ячеек столбцов.

Необязательный тэг. Значение тэга `<ColumnAlignment>`: не ожидается.

Если тэг `<ColumnAlignment>` отсутствует, то для атрибута `Value` используется значение NotSet.

```xml
<ColumnAlignment Value="NotSet" />
```

#### Атрибуты тэга `<ColumnAlignment>` <a href="#attributes_tag_column_alignment" id="attributes_tag_column_alignment"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="499.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается название одного из <a href="timetable.md#column_alignment_types">типов положения содержимого ячейки</a> столбца.</p></td></tr></tbody></table>

#### Типы положения содержимого ячейки столбца <a href="#column_alignment_types" id="column_alignment_types"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="499.3333333333333"></th></tr></thead><tbody><tr><td align="center">NotSet</td><td>Не установлено</td></tr><tr><td align="center">TopLeft</td><td>Содержимое выравнивается по верхнему краю в вертикальном направлении и по левому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">TopCenter</td><td>Содержимое выравнивается по верхнему краю в вертикальном направлении и по центру ячейки</td></tr><tr><td align="center">TopRight</td><td>Содержимое выравнивается по верхнему краю в вертикальном направлении и по правому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">MiddleLeft</td><td>Содержимое выравнивается вертикально по середине и горизонтально по левому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">MiddleCenter</td><td>Содержимое выравнивается по вертикальному и горизонтальному центру ячейки</td></tr><tr><td align="center">MiddleRight</td><td>Содержимое выравнивается вертикально по середине и горизонтально по правому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">BottomLeft</td><td>Содержимое выравнивается по нижнему краю в вертикальном направлении и по левому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">BottomCenter</td><td>Содержимое выравнивается по нижнему краю в вертикальном направлении и по центру ячейки</td></tr><tr><td align="center">BottomRight</td><td>Содержимое выравнивается по нижнему краю в вертикальном направлении и по правому краю ячейки в горизонтальном направлении</td></tr></tbody></table>

### ColumnHeaderAlignment <a href="#column_header_alignment" id="column_header_alignment"></a>

Название типа положения содержимого заголовков столбцов.

Необязательный тэг. Значение тэга `<ColumnHeaderAlignment>`: не ожидается.

Если тэг `<ColumnHeaderAlignment>` отсутствует, то для атрибута `Value` используется значение NotSet.

```xml
<ColumnHeaderAlignment Value="NotSet" />
```

#### Атрибуты тэга `<ColumnHeaderAlignment>` <a href="#attributes_tag_column_header_alignment" id="attributes_tag_column_header_alignment"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="499.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается название одного из <a href="timetable.md#column_alignment_types">типов положения содержимого ячейки</a> столбца.</p></td></tr></tbody></table>

### DateStart <a href="#date_start" id="date_start"></a>

Начальная дата периода, начиная с которой интервалы времени будут отображаться в таблице.

Обязательный тэг. Ожидается значение даты/времени.

```xml
<DateStart>01.05.2014</DateStart>
```

### DateFinish <a href="#date_finish" id="date_finish"></a>

Конечная дата периода, после которой интервалы времени перестают отображаться в таблице.

Обязательный тэг. Ожидается значение даты/времени.

```xml
<DateFinish>01.06.2014</DateFinish>
```

### Data <a href="#data" id="data"></a>

Элементы, временные интервалы, относящиеся к элементам, и цвета временных интервалов.

Обязательный тэг. Ожидается соединение с данными с тремя таблицами: 1-ая - с двумя полями, 2-ая - с двумя или четырьмя, 3-я - с семью или восьмью.

Первая таблица соответствует списку элементов: первое поле будет соответствовать идентификатору элемента, второе - его отображаемому значению.

Второй вариант интерпретации полей для таблицы элементов: первое поле будет соответствовать идентификатору элемента, второе - его отображаемому значению, третье - идентификатору цвета фона ячеек строки по умолчанию.

Вторая таблица соответствует цветам временных интервалов: первое поле будет соответствовать идентификатору цвета, второе - системному названию цвета в среде .NET (например, "Red", "Yellow" и другие).

Второй вариант интерпретации полей для таблицы цветов: первое поле будет соответствовать идентификатору цвета, второе - красной составляющей цвета, третье - зеленой, четвертое - синей.

Третья таблица соответствует временным интервалам: первое поле будет соответствовать идентификатору интервала времени, второе - идентификатору элемента, к которому относится данный интервал, третье - тексту, который будет расположен в первой ячейке таблицы, куда попадет интервал, четвертое - всплывающей подсказке, которая также будет расположена в первой ячейке, с которой начинается интервал, пятое - дате начала интервала, шестое - дате окончания интервала, седьмое - идентификатору цвета интервала, восьмое - признак отображения отметки на интервале в виде восклицательного знака (при пустом значении отметка отображается при наличии всплывающей подсказки).

В таблице временных интервалов восьмое поле является необязательным: при его отсутствии отметка в виде восклицательного знака на интервале отображается при наличии всплывающей подсказки.

```xml
<Data>
  <DataConnection SourceDataConnection="DataPrimaryGetDataConnection">
    <SourceQuery Name="Items">
      <Fields>
        <Field Name="ItemId" />
        <Field Name="Title" />
        <Field Name="ColorId" />
      </Fields>
    </SourceQuery>
    <SourceQuery Name="Colors">
      <Fields>
        <Field Name="ColorId" />
        <Field Name="Red" />
        <Field Name="Green" />
        <Field Name="Blue" />
      </Fields>
    </SourceQuery>
    <SourceQuery Name="Intervals">
      <Fields>
        <Field Name="IntervalId" />
        <Field Name="ItemId" />
        <Field Name="Text" />
        <Field Name="Hint" />
        <Field Name="IntervalDateStart" />
        <Field Name="IntervalDateFinish" />
        <Field Name="ColorId" />
        <Field Name="HasMark" />
      </Fields>
    </SourceQuery>
  </DataConnection>
</Data>
```

### Interval <a href="#interval" id="interval"></a>

Настройки интервала времени одного столбца таблицы.

Обязательный тэг. Значение тэга `<Interval>`: не ожидается.

```xml
<Interval Type="Days" Value="1" TitleFormat="dd" />
```

#### Атрибуты тэга `<Interval>` <a href="#attributes_tag_interval" id="attributes_tag_interval"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="499.3333333333333"></th></tr></thead><tbody><tr><td align="center">Type</td><td><p>Тип единиц измерения интервала столбца.</p><p></p><p>Обязательный атрибут. Ожидается название одного из <a href="timetable.md#interval_types">типов единиц измерения</a> интервала столбца.</p></td></tr><tr><td align="center">Value</td><td><p>Количество единиц времени выбранного типа в интервале столбца.</p><p></p><p>Обязательный атрибут. Ожидается положительное целочисленное значение.</p></td></tr><tr><td align="center">TitleFormat</td><td><p>Формат вывода единиц времени выбранного типа в интервале столбца (например, "HH:mm").</p><p></p><p>Обязательный атрибут. Любое значение будет переведено в текстовое.</p></td></tr></tbody></table>

#### Типы единиц измерения интервала <a href="#interval_types" id="interval_types"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="499.3333333333333"></th></tr></thead><tbody><tr><td align="center">Seconds</td><td>Секунды</td></tr><tr><td align="center">Minutes</td><td>Минуты</td></tr><tr><td align="center">Hours</td><td>Часы</td></tr><tr><td align="center">Days</td><td>Дни</td></tr><tr><td align="center">Months</td><td>Месяцы</td></tr><tr><td align="center">Years</td><td>Годы</td></tr></tbody></table>

### MultiSelect <a href="#multi_select" id="multi_select"></a>

Признак, определяющий, может ли пользователь выделять ячейки одновременно для нескольких элементов (в нескольких строках таблицы).

Необязательный тэг. Ожидается логическое значение.

```xml
<MultiSelect>False</MultiSelect>
```

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### RowHeight <a href="#get_row_height" id="get_row_height"></a>

Возвращает высоту строк с данными в таблице.

```xml
<Object Name="TimeTableName">
  <Property Name="RowHeight" />
</Object>
```

### ColumnHeadersHeight <a href="#get_column_headers_height" id="get_column_headers_height"></a>

Возвращает высоту "шапки" таблицы.

```xml
<Object Name="TimeTableName">
  <Property Name="ColumnHeadersHeight" />
</Object>
```

### ColumnHeadersVisible <a href="#get_column_headers_visible" id="get_column_headers_visible"></a>

Возвращает признак, определяющий, показывать или нет "шапку" таблицы.

```xml
<Object Name="TimeTableName">
  <Property Name="ColumnHeadersVisible" />
</Object>

```

### RowHeadersWidth <a href="#get_row_headers_width" id="get_row_headers_width"></a>

Возвращает ширину "нулевого" столбца таблицы, где расположены названия элементов.

```xml
<Object Name="TimeTableName">
  <Property Name="RowHeadersWidth" />
</Object>
```

### RowHeadersVisible <a href="#get_row_headers_visible" id="get_row_headers_visible"></a>

Возвращает признак, определяющий, показывать или нет "нулевой" столбец таблицы, где расположены названия элементов.

```xml
<Object Name="TimeTableName">
  <Property Name="RowHeadersVisible" />
</Object>
```

### BackgroundColor <a href="#get_background_color" id="get_background_color"></a>

Возвращает имя цвета фона таблицы.

```xml
<Object Name="TimeTableName">
  <Property Name="BackgroundColor" />
</Object>
```

### BorderStyle <a href="#get_border_style" id="get_border_style"></a>

Возвращает название типа границ таблицы.

```xml
<Object Name="TimeTableName">
  <Property Name="BorderStyle" />
</Object>
```

### CellBorderStyle <a href="#get_cell_border_style" id="get_cell_border_style"></a>

Возвращает название стиля границ ячеек в таблице.

```xml
<Object Name="TimeTableName">
  <Property Name="CellBorderStyle" />
</Object>
```

### AutoSizeRowsMode <a href="#get_auto_size_rows_mode" id="get_auto_size_rows_mode"></a>

Возвращает название типа автоматического изменения высот строк таблицы.

```xml
<Object Name="TimeTableName">
  <Property Name="AutoSizeRowsMode" />
</Object>
```

### VerticalScrollOffset <a href="#get_vertical_scroll_offset" id="get_vertical_scroll_offset"></a>

Возвращает величину смещения полосы вертикальной прокрутки таблицы в пикселях.

```xml
<Object Name="TimeTableName">
  <Property Name="VerticalScrollOffset" />
</Object>
```

### HorizontalScrollOffset <a href="#get_horizontal_scroll_offset" id="get_horizontal_scroll_offset"></a>

Возвращает величину смещения полосы горизонтальной прокрутки таблицы в пикселях.

```xml
<Object Name="TimeTableName">
  <Property Name="HorizontalScrollOffset" />
</Object>
```

### ColumnWidth <a href="#get_column_width" id="get_column_width"></a>

Возвращает ширину столбцов.

```xml
<Object Name="TimeTableName">
  <Property Name="ColumnWidth" />
</Object>
```

### ColumnAlignment <a href="#get_column_alignment" id="get_column_alignment"></a>

Возвращает название типа положения содержимого ячеек столбцов.

```xml
<Object Name="TimeTableName">
  <Property Name="ColumnAlignment" />
</Object>
```

### ColumnHeaderAlignment <a href="#get_column_header_alignment" id="get_column_header_alignment"></a>

Возвращает название типа положения содержимого заголовков столбцов.

```xml
<Object Name="TimeTableName">
  <Property Name="ColumnHeaderAlignment" />
</Object>
```

### DateStart <a href="#get_date_start" id="get_date_start"></a>

Возвращает начальную дату периода, начиная с которой интервалы времени будут отображаться в таблице.

```xml
<Object Name="TimeTableName">
  <Property Name="DateStart" />
</Object>
```

### DateFinish <a href="#get_date_finish" id="get_date_finish"></a>

Возвращает конечную дату периода, после которой интервалы времени перестают отображаться в таблице.

```xml
<Object Name="TimeTableName">
  <Property Name="DateFinish" />
</Object>
```

### IntervalType <a href="#get_interval_type" id="get_interval_type"></a>

Возвращает название типа единиц измерения интервала столбца.

```xml
<Object Name="TimeTableName">
  <Property Name="IntervalType" />
</Object>
```

### IntervalValue <a href="#get_interval_value" id="get_interval_value"></a>

Возвращает количество единиц времени выбранного типа в интервале столбца.

```xml
<Object Name="TimeTableName">
  <Property Name="IntervalValue" />
</Object>
```

### IntervalTitleFormat <a href="#get_interval_title_format" id="get_interval_title_format"></a>

Возвращает формат вывода единиц времени выбранного типа в интервале столбца.

```xml
<Object Name="TimeTableName">
  <Property Name="IntervalTitleFormat" />
</Object>
```

### MultiSelect <a href="#get_multi_select" id="get_multi_select"></a>

Возвращает признак, определяющий, может ли пользователь выделять ячейки одновременно для нескольких элементов (в нескольких строках таблицы).

```xml
<Object Name="TimeTableName">
  <Property Name="MultiSelect" />
</Object>
```

### SelectedDateStart <a href="#get_selected_date_start" id="get_selected_date_start"></a>

Возвращает дату, соответствующую началу самой левой среди выделенных ячеек таблицы.

```xml
<Object Name="TimeTableName">
  <Property Name="SelectedDateStart" />
</Object>
```

### SelectedDateFinish <a href="#get_selected_date_finish" id="get_selected_date_finish"></a>

Возвращает дату, соответствующую окончанию самой правой среди выделенных ячеек таблицы.

```xml
<Object Name="TimeTableName">
  <Property Name="SelectedDateFinish" />
</Object>
```

### SelectedItemsCount <a href="#get_selected_items_count" id="get_selected_items_count"></a>

Возвращает количество элементов, выделенных в таблице (элемент считается выделенным, если выделена хотя бы одна ячейка в строке, соответствующей этому элементу).

```xml
<Object Name="TimeTableName">
  <Property Name="SelectedItemsCount" />
</Object>
```

### SelectedItemId <a href="#get_selected_item_id" id="get_selected_item_id"></a>

Возвращает идентификатор одного из выделенных элементов таблицы (элемент считается выделенным, если выделена хотя бы одна ячейка в строке, соответствующей этому элементу).

```xml
<Object Name="TimeTableName">
  <Property Name="SelectedItemId" />
</Object>
```

### SelectedItemIds <a href="#get_selected_item_ids" id="get_selected_item_ids"></a>

Возвращает массив идентификаторов всех выделенных элементов таблицы (элемент считается выделенным, если выделена хотя бы одна ячейка в строке, соответствующей этому элементу).

```xml
<Object Name="TimeTableName">
  <Property Name="SelectedItemIds" />
</Object>
```

### SelectedIntervalsCount <a href="#get_selected_intervals_count" id="get_selected_intervals_count"></a>

Возвращает количество интервалов времени, выделенных в таблице (интервал времени считается выделенным, если выделена хотя бы одна ячейка, в которую он попадает).

```xml
<Object Name="TimeTableName">
  <Property Name="SelectedIntervalsCount" />
</Object>
```

### SelectedIntervalId <a href="#get_selected_interval_id" id="get_selected_interval_id"></a>

Возвращает идентификатор одного из выделенных интервалов времени (интервал времени считается выделенным, если выделена хотя бы одна ячейка, в которую он попадает).

```xml
<Object Name="TimeTableName">
  <Property Name="SelectedIntervalId" />
</Object>
```

### SelectedIntervalIds <a href="#get_selected_interval_ids" id="get_selected_interval_ids"></a>

Возвращает массив идентификаторов всех выделенных интервалов времени (интервал времени считается выделенным, если выделена хотя бы одна ячейка, в которую он попадает).

```xml
<Object Name="TimeTableName">
  <Property Name="SelectedIntervalIds" />
</Object>
```

### SelectedCellsFilled <a href="#selected_cells_filled" id="selected_cells_filled"></a>

Возвращает признак, определяющий, заполнены ли временными интервалами выделенные ячейки полностью.

```xml
<Object Name="TimeTableName">
  <Property Name="SelectedCellsFilled" />
</Object>
```

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

### RowHeight <a href="#set_row_height" id="set_row_height"></a>

Задает высоту строк с данными в таблице.

Ожидается целочисленное значение.

```xml
<Object Name="TimeTableName">
  <Property Name="RowHeight">20</Property>
</Object>
```

### ColumnHeadersHeight <a href="#set_column_headers_height" id="set_column_headers_height"></a>

Задает высоту "шапки" таблицы.

Ожидается целочисленное значение.

```xml
<Object Name="TimeTableName">
  <Property Name="ColumnHeadersHeight">20</Property>
</Object>
```

### ColumnHeadersVisible <a href="#set_column_headers_visible" id="set_column_headers_visible"></a>

Задает признак, определяющий, показывать или нет "шапку" таблицы.

Ожидается логическое значение.

```xml
<Object Name="TimeTableName">
  <Property Name="ColumnHeadersVisible">True</Property>
</Object>
```

### RowHeadersWidth <a href="#set_row_headers_width" id="set_row_headers_width"></a>

Задает ширину "нулевого" столбца таблицы, где расположены названия элементов.

Ожидается целочисленное значение.

```xml
<Object Name="TimeTableName">
  <Property Name="RowHeadersWidth">200</Property>
</Object>
```

### RowHeadersVisible <a href="#set_row_headers_visible" id="set_row_headers_visible"></a>

Задает признак, определяющий, показывать или нет "нулевой" столбец таблицы, где расположены названия элементов.

Ожидается логическое значение.

```xml
<Object Name="TimeTableName">
  <Property Name="RowHeadersVisible">False</Property>
</Object>
```

### BackgroundColor <a href="#set_background_color" id="set_background_color"></a>

Задает имя цвета фона таблицы.

Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

```xml
<Object Name="TimeTableName">
  <Property Name="BackgroundColor">BackgroundColor</Property>
</Object>
```

### BorderStyle <a href="#set_border_style" id="set_border_style"></a>

Задает название типа границ таблицы.

Ожидается название одного из типов границ таблицы.

```xml
<Object Name="TimeTableName">
  <Property Name="BorderStyle">Fixed3D</Property>
</Object>
```

### CellBorderStyle <a href="#set_cell_border_style" id="set_cell_border_style"></a>

Задает название стиля границ ячеек в таблице.

Ожидается название одного из стилей границ ячеек в таблице.

```xml
<Object Name="TimeTableName">
  <Property Name="CellBorderStyle">SingleHorizontal</Property>
</Object>
```

### AutoSizeRowsMode <a href="#set_auto_size_rows_mode" id="set_auto_size_rows_mode"></a>

Задает название типа автоматического изменения высот строк таблицы.

Ожидается название одного из типов автоматического изменения высот строк таблицы.

```xml
<Object Name="TimeTableName">
  <Property Name="AutoSizeRowsMode">AllCells</Property>
</Object>
```

### AutoSize <a href="#set_auto_size" id="set_auto_size"></a>

Единоразово устанавливает ширину и высоту таблицы, сворачивая или разворачивая её таким образом, чтобы в зоне видимости оказались все её строки и столбцы без полос прокрутки.

Значение тэга `<Property>`: не ожидается.

```xml
<Object Name="TimeTableName"
  <Property Name="AutoSize" />
</Object>
```

### DateStart <a href="#set_date_start" id="set_date_start"></a>

Задает начальную дату периода, начиная с которой интервалы времени будут отображаться в таблице.

Ожидается значение даты/времени.

```xml
<Object Name="TimeTableName">
  <Property Name="DateStart">01.06.2014</Property>
</Object>
```

### DateFinish <a href="#set_date_finish" id="set_date_finish"></a>

Задает конечную дату периода, после которой интервалы времени перестают отображаться в таблице.

Ожидается значение даты/времени.

```xml
<Object Name="TimeTableName">
  <Property Name="DateFinish">01.07.2014</Property>
</Object>
```

### MultiSelect <a href="#set_multi_select" id="set_multi_select"></a>

Задает признак, определяющий, может ли пользователь выделять ячейки одновременно для нескольких элементов (в нескольких строках таблицы).

Ожидается логическое значение.

```xml
<Object Name="TimeTableName">
  <Property Name="MultiSelect">True</Property>
</Object>
```
