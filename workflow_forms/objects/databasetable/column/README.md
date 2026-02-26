---
description: Описание тэгов, общих для всех типов столбцов таблицы DatabaseTable
---

# Column

## Шаблон столбцов DatabaseTable <a href="#template_databasetable" id="template_databasetable"></a>

Перечень возможных общих тэгов для всех типов столбцов:

```xml
<Column Name="" Type="" Assembly="DatabaseTableColumnControls">
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
  <!--Тэги, специфичные для определенного типа столбца-->
</Column>
```

## Тэги, общие для всех столбцов таблицы <a href="#common_columns_tags" id="common_columns_tags"></a>

### Title <a href="#column_title" id="column_title"></a>

Заголовок столбца.

Необязательный тэг. Любое значение будет переведено в текстовое.

По умолчанию используется название столбца из атрибута `Name` тэга `<Column>`.

```xml
<Title>Заголовок</Title>
```

### Width <a href="#column_width" id="column_width"></a>

Ширина столбца.

Необязательный тэг. Ожидается целочисленное значение.

По умолчанию используется стандартное значение .NET.

```xml
<Width>100</Width>
```

### MinimumWidth <a href="#column_minium_width" id="column_minium_width"></a>

Минимальная ширина столбца.

Необязательный тэг. Ожидается целочисленное значение.

По умолчанию используется стандартное значение .NET.

```xml
<MinimumWidth>100</MinimumWidth>
```

### DisplayIndex <a href="#column_display_index" id="column_display_index"></a>

Порядок отображения столбца.

Необязательный тэг. Ожидается неотрицательное целочисленное значение.

По умолчанию используется порядок описания столбцов в таблице.

```xml
<DisplayIndex>0</DisplayIndex>
```

### Frozen <a href="#column_frozen" id="column_frozen"></a>

Признак, определяющий, будет столбец "заморожен" (видим всегда) при горизонтальной прокрутке содержимого таблицы.

Необязательный тэг. Значение тэга не ожидается.

Обязательный атрибут `Value` ожидает логическое значение. По умолчанию используется значение False.

```xml
<Frozen Value="False" />
```

### WrapMode <a href="#column_wrap_mode" id="column_wrap_mode"></a>

Признак, определяющий, будут ли в содержании ячеек столбца переносы на новую строку, если все содержание ячейки не входит в ее видимую область.

Необязательный тэг. Значение тэга не ожидается.

Обязательный атрибут `Value` ожидает логическое значение. По умолчанию используется значение False.

```xml
<WrapMode Value="False" />
```

### ReadOnly <a href="#column_read_only" id="column_read_only"></a>

Признак, определяющий, может ли пользователь изменять значения ячеек данного столбца.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<ReadOnly>False</ReadOnly>
```

### AllowSort <a href="#column_allow_sort" id="column_allow_sort"></a>

Признак, определяющий, можно ли отсортировать столбец по нажатию на его заголовок из графического интерфейса таблицы.

Необязательный тэг. Значение тэга не ожидается.

Обязательный атрибут `Value` ожидает логическое значение. По умолчанию используется значение True.

```xml
<AllowSort Value="False" />
```

### Alignment <a href="#column_alignment" id="column_alignment"></a>

Название типа положения содержимого ячейки столбца.

Необязательный тэг.&#x20;

{% hint style="info" %}
Не распространяется на столбец типа [DatabaseTableColumnCheckBox](column_check_box.md).
{% endhint %}

```xml
<Alignment Value="NotSet" />
```

Для обязательного атрибута `Value` ожидается название одного из типов положения содержимого ячейки столбца таблицы:

<table data-header-hidden><thead><tr><th width="226.6296484971982" align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">NotSet</td><td>Значение наследуется от свойства <a href="./#column_headers_alignment"><code>&#x3C;ColumnHeadersAlignment></code></a> таблицы<br>(По умолчанию)</td></tr><tr><td align="center">TopLeft</td><td>Содержимое выравнивается по верхнему краю в вертикальном направлении и по левому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">TopCenter</td><td>Содержимое выравнивается по верхнему краю в вертикальном направлении и по центру ячейки</td></tr><tr><td align="center">TopRight</td><td>Содержимое выравнивается по верхнему краю в вертикальном направлении и по правому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">MiddleLeft</td><td>Содержимое выравнивается вертикально по середине и горизонтально по левому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">MiddleCenter</td><td>Содержимое выравнивается по вертикальному и горизонтальному центру ячейки</td></tr><tr><td align="center">MiddleRight</td><td>Содержимое выравнивается вертикально по середине и горизонтально по правому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">BottomLeft</td><td>Содержимое выравнивается по нижнему краю в вертикальном направлении и по левому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">BottomCenter</td><td>Содержимое выравнивается по нижнему краю в вертикальном направлении и по центру ячейки</td></tr><tr><td align="center">BottomRight</td><td>Содержимое выравнивается по нижнему краю в вертикальном направлении и по правому краю ячейки в горизонтальном направлении</td></tr></tbody></table>

### HeaderAlignment <a href="#column_header_alignment" id="column_header_alignment"></a>

Название типа положения содержимого заголовка столбца.

Необязательный тэг.&#x20;

```xml
<HeaderAlignment Value="NotSet" />
```

Для обязательного атрибута `Value` ожидается название одного из типов положения содержимого ячейки столбца таблицы:

<table data-header-hidden><thead><tr><th width="226.6296484971982" align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">NotSet</td><td>Значение наследуется от свойства <a href="./#column_headers_alignment"><code>&#x3C;ColumnHeadersAlignment></code></a> таблицы<br>(По умолчанию)</td></tr><tr><td align="center">TopLeft</td><td>Содержимое выравнивается по верхнему краю в вертикальном направлении и по левому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">TopCenter</td><td>Содержимое выравнивается по верхнему краю в вертикальном направлении и по центру ячейки</td></tr><tr><td align="center">TopRight</td><td>Содержимое выравнивается по верхнему краю в вертикальном направлении и по правому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">MiddleLeft</td><td>Содержимое выравнивается вертикально по середине и горизонтально по левому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">MiddleCenter</td><td>Содержимое выравнивается по вертикальному и горизонтальному центру ячейки</td></tr><tr><td align="center">MiddleRight</td><td>Содержимое выравнивается вертикально по середине и горизонтально по правому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">BottomLeft</td><td>Содержимое выравнивается по нижнему краю в вертикальном направлении и по левому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">BottomCenter</td><td>Содержимое выравнивается по нижнему краю в вертикальном направлении и по центру ячейки</td></tr><tr><td align="center">BottomRight</td><td>Содержимое выравнивается по нижнему краю в вертикальном направлении и по правому краю ячейки в горизонтальном направлении</td></tr></tbody></table>

### AutoSizeMode <a href="#column_auto_size_mode" id="column_auto_size_mode"></a>

Название типа автоматического изменения ширины столбца.

Необязательный тэг.

```xml
<AutoSizeMode Value="NotSet" />
```

Для обязательного атрибута `Value` ожидается название одного из типов автоматического изменения ширины столбцов таблицы:

<table data-header-hidden><thead><tr><th width="275.7376913646473" align="center"></th><th width="488.3333333333333"></th></tr></thead><tbody><tr><td align="center">NotSet</td><td>Значение наследуется от свойства <a href="./#auto_size_columns_mode"><code>&#x3C;AutoSizeColumnsMode></code></a> таблиц<br>(По умолчанию)</td></tr><tr><td align="center">None</td><td>Нет автоматического изменения ширины столбца</td></tr><tr><td align="center">AllCells</td><td>Ширина столбца изменяется в соответствии с содержимым всех ячеек в столбце, включая ячейки заголовка</td></tr><tr><td align="center">AllCellsExceptHeader</td><td>Ширина столбца изменяется в соответствии с содержимым всех ячеек в столбце, исключая ячейки заголовка</td></tr><tr><td align="center">ColumnHeader</td><td>Ширина столбца изменяется в соответствии с содержимым заголовка столбцов</td></tr><tr><td align="center">DisplayedCells</td><td>Ширина столбца изменяется в соответствии с содержимым всех ячеек в столбце, отображаемых в текущий момент на экране, включая ячейки заголовка</td></tr><tr><td align="center">DisplayedCellsExceptHeaders</td><td>Ширина столбца изменяется в соответствии с содержимым всех ячеек в столбце, отображаемых в текущий момент на экране, исключая ячейки заголовка</td></tr><tr><td align="center">Fill</td><td>Ширина столбца изменяется так, чтобы точно заполнить ширину всей отображаемой области таблицы, с учетом наличия или отсутствия полосы горизонтальной прокрутки</td></tr></tbody></table>

### HeaderBackColor <a href="#column_header_back_color" id="column_header_back_color"></a>

Цвет фона заголовка столбца.

Необязательный тэг. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется стандартное значение .NET.

```xml
<HeaderBackColor>HeaderBackColor</HeaderBackColor>
```

### HeaderForeColor <a href="#column_header_fore_color" id="column_header_fore_color"></a>

Цвет шрифта заголовка столбца.

Необязательный тэг. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется стандартное значение .NET.

```xml
<HeaderForeColor>HeaderForeColor</HeaderForeColor>
```

### HeaderSelectionBackColor <a href="#column_header_selection_back_color" id="column_header_selection_back_color"></a>

Цвет фона заголовка столбца выделенной ячейки.

Необязательный тэг. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется стандартное значение .NET.

```xml
<HeaderForeColor>HeaderForeColor</HeaderForeColor>
```

### BackColor <a href="#column_back_color" id="column_back_color"></a>

Цвет фона ячеек столбца.

Необязательный тэг. Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется стандартное значение .NET.

```xml
<BackColor>BackColor</BackColor>
```

### ForeColor <a href="#column_fore_color" id="column_fore_color"></a>

Цвет шрифта ячеек столбца.

Необязательный тэг. Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется стандартное значение .NET.

```xml
<ForeColor>ForeColor</ForeColor>
```

### Visible <a href="#column_visible" id="column_visible"></a>

Признак видимости столбца.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение True.

```xml
<Visible>True</Visible>
```

### Hint <a href="#column_hint" id="column_hint"></a>

Подсказка, всплывающая на заголовке столбца.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Hint>Подсказка</Hint>
```

### ToolTipColumnName <a href="#tool_tip_column_name" id="tool_tip_column_name"></a>

Имя столбца, значение ячейки которого будет использоваться во всплывающей подсказке при наведении курсора мыши на ячейку той же строки в настраиваемом столбце.

Необязательный тэг. Любое значение будет переведено в текстовое.

По умолчанию для подсказки используется значение из текущего столбца.

```xml
<ToolTipColumnName>ColumnName</ToolTipColumnName>
```

### DataType <a href="#column_data_type" id="column_data_type"></a>

Настройки форматированного вывода значений в ячейках столбца.

Необязательный тэг. Значение тэга не ожидается.

```xml
<DataType Type="DataType" />
```

Для обязательного атрибута `Type` ожидается название одного из [типов данных](/broken/pages/-MaRtBVKMO4VR0KCghVx).

{% hint style="warning" %}
Остальные атрибуты тэга зависят от указанного типа данных.
{% endhint %}

### Sorting <a href="#column_sorting" id="column_sorting"></a>

Правила автоматической сортировки столбца.

Необязательный тэг. В качестве значения ожидаются тэги `<SortOrder>` и `<ColumnOrder>`.

```xml
<Sorting>
  <SortOrder Type="Asc" />
  <ColumnOrder Order="1" />
</Sorting>
```

Необязательный тэг `<SortOrder>` задает тип сортировки:

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Asc</td><td><p>По возрастанию</p><p>(По умолчанию)</p></td></tr><tr><td align="center">Desc</td><td>По убыванию</td></tr></tbody></table>

Обязательный тэг `<ColumnOrder>` задает приоритет столбца при сортировке. Чем значение меньше, тем выше приоритет.

### Filter <a href="#column_filter" id="column_filter"></a>

Правила фильтрации (отображения) строк в таблице.

Необязательный тэг. Значение тэга любое значение.

```xml
<Filter AutoFill="True" FilterNullValue="False">
  <Object Name="ObjectComboBox" />
</Filter>
```

Необязательный атрибут `AutoFill` - признак, определяющий, будет ли передан список уникальных значений ячеек настраиваемого столбца в свойство ValueList объекта, указанного в тэге `<Filter>`.

Ожидается логическое значение. По умолчанию используется значение True.

{% hint style="warning" %}
Список уникальных значений будет отправлен только в тот объект формы, который имеет set-проперти ValueList. Во всех остальных случаях атрибут `AutoFill` ни на что не влияет.
{% endhint %}

Необязательный атрибут `FilterNullValue` - признак, определяющий, будет ли осуществляться фильтрация столбца, если фильтр будет иметь значение NULL.

Ожидается логическое значение. По умолчанию используется значение False.

### Substitution <a href="#column_substitution" id="column_substitution"></a>

Подстановка в ячейки столбца значений, зависящих от значений в других столбцах.

Необязательный тэг. Ожидается таблица с двумя столбцами. Первый столбец должен содержать реальные значения элементов, а второй - их отображаемое значение.

```xml
<Substitution SourceColumn="SourceColumnName">
  <DataConnection SourceDataConnection="SourceDataConnectionName">
    <Fields>
      <Field Name="Field1Name" />
      <Field Name="Field2Name" />
    </Fields>
  </DataConnection>
</Substitution>
```

В обязательном атрибуте `SourceColumn` ожидается имя одного из столбцов редактируемой таблицы DatabaseTable. Значение из ячейки этого столбца будет использоваться для поиска значения в матрице, указанной в тэге `<Substitution>`. Найденное значение будет подставляться в ячейку настраиваемого столбца. Подстановка происходит построчно.

### DefaultNewRowValue <a href="#column_default_new_row_value" id="column_default_new_row_value"></a>

Значение по умолчанию для ячейки столбца при добавлении новой строке в таблицу.

Необязательный тэг. Ожидается любое значение.

```xml
<DefaultNewRowValue>Value</DefaultNewRowValue>
```

### AutoFill <a href="#column_auto_fill" id="column_auto_fill"></a>

Автоматическое заполнение значений в ячейках столбца.

Необязательный тэг. Значение тэга не ожидается.

```xml
<AutoFill Type="RowNumber" />
```

Обязательный атрибут `Type` задает тип автоматического заполнения. Ожидается название одного из типов:

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">RowNumber</td><td>Номер по порядку</td></tr></tbody></table>

### Calculate <a href="#column_calculate" id="column_calculate"></a>

Задает выражение для вычисляемого столбца.

Необязательный тэг. В качестве значения ожидаются тэги  `<Expression>` и `<Items>`.

```xml
<Calculate>
  <Expression>(ColumnName1 * ColumnName2 + {0}) * {1}</Expression>
  <Items>
    <Item>100</Item>
    <Item>
      <Object Name="ObjectTextBox" />
    </Item>
  </Items>
</Calculate>
```

Обязательный тэг `<Expression>` задает выражение для вычисления значений настраиваемого столбца. Для каждой строки значение вычисляется отдельно. Выражение поддерживает обращение к значениям в других столбцах через указание имени столбца, а так же обращение к элементам, перечисленным в тэге `<Items>`, по их индексу - {N}.

{% hint style="info" %}
Все конструкции, поддерживаемые в выражении вычисляемого столбца, можно найти по [ссылке](https://docs.microsoft.com/en-us/dotnet/api/system.data.datacolumn.expression?redirectedfrom=MSDN\&view=net-6.0#System_Data_DataColumn_Expression).
{% endhint %}

Необязательный тэг `<Items>` ожидает список тэгов `<Item>` - список переменных для подстановки в выражение. Для необязательного тэга `<Item>` ожидается любое значение.

### ManagementMode <a href="#column_management_mode" id="column_management_mode"></a>

Используется, чтобы указать режим управления отображением столбца.

Необязательный тэг. Ожидается название одного из режимов управления:

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Allowed</td><td>Разрешено изменять порядок и видимость столбца<br>(По умолчанию)</td></tr><tr><td align="center">NotAllowed</td><td>Запрещено изменять порядок и видимость столбца</td></tr><tr><td align="center">PartiallyAllowed</td><td>Разрешено изменять порядок, запрещено изменять видимость столбца</td></tr></tbody></table>

```xml
<ManagementMode>Allowed</ManagementMode>
```
