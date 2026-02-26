---
description: Графический объект; таблица, которая работает с данными базы.
---

# DatabaseTable

## Шаблон DatabaseTable <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

<pre class="language-xml"><code class="lang-xml">&#x3C;MyObject Name="" Type="DatabaseTable" Assembly="ComplexControls" ChangeForm="">
  &#x3C;!--Тэги, общие для всех графических объектов-->
  &#x3C;Top>&#x3C;/Top>
  &#x3C;Left>&#x3C;/Left>
  &#x3C;Height>&#x3C;/Height>
  &#x3C;Width>&#x3C;/Width>
  &#x3C;FontStyle>&#x3C;/FontStyle>
  &#x3C;ForeColor>&#x3C;/ForeColor>
  &#x3C;BackColor>&#x3C;/BackColor>
  &#x3C;Enabled>&#x3C;/Enabled>
  &#x3C;Visible>&#x3C;/Visible>
  &#x3C;Hint>&#x3C;/Hint>
  &#x3C;Change User="" Source="" ValueSet="" />
  &#x3C;!--Тэги, специфичные для DatabaseTable-->
  &#x3C;RowHeight Value="" />
  &#x3C;ColumnHeadersHeight Value="" />
  &#x3C;ColumnHeadersVisible Value="" />
  &#x3C;RowHeadersWidth Value="" />
  &#x3C;RowHeadersVisible Value="" />
  &#x3C;BackgroundColor Value="" />
  &#x3C;BorderStyle Value="" />
  &#x3C;CellBorderStyle Value="" />
  &#x3C;HideSelection Value="" />
  &#x3C;SelectionColor Name="" FadingRatio="" />
  &#x3C;AllowInsert>&#x3C;/AllowInsert>
  &#x3C;AllowUpdate>&#x3C;/AllowUpdate>
  &#x3C;AllowDelete>&#x3C;/AllowDelete>
  &#x3C;MultiSelect Value="" />
  &#x3C;ScrollBars Value="" />
  &#x3C;SelectionMode Value="" />
  &#x3C;EditMode Value="" />
  &#x3C;AllowResizeColumns Value="" />
  &#x3C;AllowOrderColumns Value="" />
  &#x3C;AllowResizeRows Value="" />
  &#x3C;AutoSizeRowsMode Value="" />
  &#x3C;AutoSizeColumnsMode Value="" />
  &#x3C;AllowFilterColumns Value="" />
  &#x3C;ColumnHeadersHeightSizeMode Value="" />
  &#x3C;ColumnHeadersAlignment Value="" />
  &#x3C;ShowCellHints Value="" />
  &#x3C;ContextMenu Name="" MultiSelection="" />
  &#x3C;ColumnContextMenuBackColor Name="" />
  &#x3C;ColumnContextMenuForeColor Name="" />
  &#x3C;Formatting>
    &#x3C;BackColor Name="">
      &#x3C;Columns>
        &#x3C;Column Name="" />
        &#x3C;Column Name="" />
      &#x3C;/Columns>
      &#x3C;Expression>&#x3C;/Expression>
      &#x3C;Items>
        &#x3C;Item>&#x3C;/Item>
        &#x3C;Item>&#x3C;/Item>
      &#x3C;/Items>
    &#x3C;/BackColor>
    &#x3C;BackColor>
      &#x3C;Color>&#x3C;/Color>
      &#x3C;Columns>
        &#x3C;Column Name="" />
        &#x3C;Column Name="" />
      &#x3C;/Columns>
      &#x3C;Expression>&#x3C;/Expression>
      &#x3C;Items>
        &#x3C;Item>&#x3C;/Item>
        &#x3C;Item>&#x3C;/Item>
      &#x3C;/Items>
    &#x3C;/BackColor>
    &#x3C;BackColor>
      &#x3C;ColorFromColumnValue>&#x3C;/ColorFromColumnValue>
      &#x3C;Columns>
        &#x3C;Column Name="" />
        &#x3C;Column Name="" />
      &#x3C;/Columns>
      &#x3C;Expression>&#x3C;/Expression>
      &#x3C;Items>
        &#x3C;Item>&#x3C;/Item>
        &#x3C;Item>&#x3C;/Item>
      &#x3C;/Items>
    &#x3C;/BackColor>
    &#x3C;ForeColor Name="">
      &#x3C;Columns>
        &#x3C;Column Name="" />
        &#x3C;Column Name="" />
      &#x3C;/Columns>
      &#x3C;Expression>&#x3C;/Expression>
      &#x3C;Items>
        &#x3C;Item>&#x3C;/Item>
        &#x3C;Item>&#x3C;/Item>
      &#x3C;/Items>
    &#x3C;/ForeColor>
    &#x3C;ForeColor>
      &#x3C;Color>&#x3C;/Color>
      &#x3C;Columns>
        &#x3C;Column Name="" />
        &#x3C;Column Name="" />
      &#x3C;/Columns>
      &#x3C;Expression>&#x3C;/Expression>
      &#x3C;Items>
        &#x3C;Item>&#x3C;/Item>
        &#x3C;Item>&#x3C;/Item>
      &#x3C;/Items>
    &#x3C;/ForeColor>
    &#x3C;ForeColor>
      &#x3C;ColorFromColumnValue>&#x3C;/ColorFromColumnValue>
      &#x3C;Columns>
        &#x3C;Column Name="" />
        &#x3C;Column Name="" />
      &#x3C;/Columns>
      &#x3C;Expression>&#x3C;/Expression>
      &#x3C;Items>
        &#x3C;Item>&#x3C;/Item>
        &#x3C;Item>&#x3C;/Item>
      &#x3C;/Items>
    &#x3C;/ForeColor>
    &#x3C;FontStyle Name="">
      &#x3C;Columns>
        &#x3C;Column Name="" />
        &#x3C;Column Name="" />
      &#x3C;/Columns>
      &#x3C;Expression>&#x3C;/Expression>
      &#x3C;Items>
        &#x3C;Item>&#x3C;/Item>
        &#x3C;Item>&#x3C;/Item>
      &#x3C;/Items>
    &#x3C;/FontStyle>
    &#x3C;Alignment>
      &#x3C;Value>&#x3C;/Value>
      &#x3C;Columns>
        &#x3C;Column Name="" />
      &#x3C;/Columns>
      &#x3C;Expression>&#x3C;/Expression>
    &#x3C;/Alignment>
    &#x3C;Alignment Value="">
      &#x3C;Columns>
        &#x3C;Column Name="" />
      &#x3C;/Columns>
      &#x3C;Expression>&#x3C;/Expression>
    &#x3C;/Alignment>
  &#x3C;/Formatting>
  &#x3C;SourceDataConnection Name="" Query=""/>
  &#x3C;SaveOnFormClose Columns="" />
  &#x3C;Columns>
<strong>    &#x3C;Column Name="" Type="DatabaseTableColumnTextBox" Assembly="DatabaseTableColumnControls" >
</strong>      &#x3C;Title>&#x3C;/Title> 
      &#x3C;Width>&#x3C;/Width>
      &#x3C;DisplayIndex>&#x3C;/DisplayIndex>
      &#x3C;Frozen Value="" />
      &#x3C;WrapMode Value="" />
      &#x3C;ReadOnly>&#x3C;/ReadOnly> 
      &#x3C;AllowSort Value="" />
      &#x3C;Alignment Value="" />
      &#x3C;HeaderAlignment Value="" />
      &#x3C;AutoSizeMode Value="" />
      &#x3C;HeaderBackColor>&#x3C;/HeaderBackColor>
      &#x3C;BackColor>&#x3C;/BackColor>
      &#x3C;ForeColor>&#x3C;/ForeColor>
      &#x3C;Visible>&#x3C;/Visible>
      &#x3C;Hint>&#x3C;/Hint>
      &#x3C;DataType DataType="" />
      &#x3C;Substitution SourceColumn="">
        &#x3C;DataConnection SourceDataConnection="">
          &#x3C;Fields>
            &#x3C;Field Name="" />
            &#x3C;Field Name="" />
          &#x3C;/Fields>
        &#x3C;/DataConnection>
      &#x3C;/Substitution>
      &#x3C;Sorting>
        &#x3C;SortOrder Type="" />
        &#x3C;ColumnOrder Order="" />
      &#x3C;/Sorting>
      &#x3C;Filter AutoFill="" FilterNullValue="">&#x3C;/Filter>
      &#x3C;DefaultNewRowValue>&#x3C;/DefaultNewRowValue>
      &#x3C;AutoFill Type="" />
      &#x3C;Calculate>
        &#x3C;Expression>&#x3C;/Expression>
        &#x3C;Items>
          &#x3C;Item>&#x3C;/Item>
          &#x3C;Item>&#x3C;/Item>
        &#x3C;/Items>
      &#x3C;/Calculate>
      &#x3C;ManagementMode>&#x3C;/ManagementMode>
    &#x3C;/Column>
    &#x3C;Column Name="" Type="DatabaseTableColumnComboBox" Assembly="DatabaseTableColumnControls" >
      &#x3C;Title>&#x3C;/Title> 
      &#x3C;Width>&#x3C;/Width>
      &#x3C;DisplayIndex>&#x3C;/DisplayIndex>
      &#x3C;Frozen Value="" />
      &#x3C;WrapMode Value="" />
      &#x3C;ReadOnly>&#x3C;/ReadOnly> 
      &#x3C;AllowSort Value="" />
      &#x3C;Alignment Value="" />
      &#x3C;HeaderAlignment Value="" />
      &#x3C;AutoSizeMode Value="" />
      &#x3C;HeaderBackColor>&#x3C;/HeaderBackColor>
      &#x3C;BackColor>&#x3C;/BackColor>
      &#x3C;ForeColor>&#x3C;/ForeColor>
      &#x3C;Visible>&#x3C;/Visible>
      &#x3C;Hint>&#x3C;/Hint>
      &#x3C;DataType DataType="" />
      &#x3C;Substitution SourceColumn="">
        &#x3C;DataConnection SourceDataConnection="">
          &#x3C;Fields>
            &#x3C;Field Name="" />
            &#x3C;Field Name="" />
          &#x3C;/Fields>
        &#x3C;/DataConnection>
      &#x3C;/Substitution>
      &#x3C;Sorting>
        &#x3C;SortOrder Type="" />
        &#x3C;ColumnOrder Order="" />
      &#x3C;/Sorting>
      &#x3C;Filter AutoFill="" FilterNullValue="">&#x3C;/Filter>
      &#x3C;DefaultNewRowValue>&#x3C;/DefaultNewRowValue>
      &#x3C;AutoFill Type="" />
      &#x3C;Calculate>
        &#x3C;Expression>&#x3C;/Expression>
        &#x3C;Items>
          &#x3C;Item>&#x3C;/Item>
          &#x3C;Item>&#x3C;/Item>
        &#x3C;/Items>
      &#x3C;/Calculate>
      &#x3C;Sorted Value="" />
      &#x3C;ValueList>&#x3C;/ValueList>
      &#x3C;ManagementMode>&#x3C;/ManagementMode>
    &#x3C;/Column>
    &#x3C;Column Name="" Type="DatabaseTableColumnCheckBox" Assembly="DatabaseTableColumnControls" >
      &#x3C;Title>&#x3C;/Title> 
      &#x3C;Width>&#x3C;/Width>
      &#x3C;DisplayIndex>&#x3C;/DisplayIndex>
      &#x3C;Frozen Value="" />
      &#x3C;WrapMode Value="" />
      &#x3C;ReadOnly>&#x3C;/ReadOnly> 
      &#x3C;AllowSort Value="" />
      &#x3C;Alignment Value="" />
      &#x3C;HeaderAlignment Value="" />
      &#x3C;AutoSizeMode Value="" />
      &#x3C;HeaderBackColor>&#x3C;/HeaderBackColor>
      &#x3C;BackColor>&#x3C;/BackColor>
      &#x3C;ForeColor>&#x3C;/ForeColor>
      &#x3C;Visible>&#x3C;/Visible>
      &#x3C;Hint>&#x3C;/Hint>
      &#x3C;DataType DataType="" />
      &#x3C;Substitution SourceColumn="">
        &#x3C;DataConnection SourceDataConnection="">
          &#x3C;Fields>
            &#x3C;Field Name="" />
            &#x3C;Field Name="" />
          &#x3C;/Fields>
        &#x3C;/DataConnection>
      &#x3C;/Substitution>
      &#x3C;Sorting>
        &#x3C;SortOrder Type="" />
        &#x3C;ColumnOrder Order="" />
      &#x3C;/Sorting>
      &#x3C;Filter AutoFill="" FilterNullValue="">&#x3C;/Filter>
      &#x3C;DefaultNewRowValue>&#x3C;/DefaultNewRowValue>
      &#x3C;AutoFill Type="" />
      &#x3C;Calculate>
        &#x3C;Expression>&#x3C;/Expression>
        &#x3C;Items>
          &#x3C;Item>&#x3C;/Item>
          &#x3C;Item>&#x3C;/Item>
        &#x3C;/Items>
      &#x3C;/Calculate>
      &#x3C;ThreeState Value="" />
      &#x3C;HeaderCheckAll Value="" />
      &#x3C;ManagementMode>&#x3C;/ManagementMode>
    &#x3C;/Column>
    &#x3C;Column Name="" Type="DatabaseTableColumnDateTimePicker" Assembly="DatabaseTableColumnControls" >
      &#x3C;Title>&#x3C;/Title> 
      &#x3C;Width>&#x3C;/Width>
      &#x3C;DisplayIndex>&#x3C;/DisplayIndex>
      &#x3C;Frozen Value="" />
      &#x3C;WrapMode Value="" />
      &#x3C;ReadOnly>&#x3C;/ReadOnly> 
      &#x3C;AllowSort Value="" />
      &#x3C;Alignment Value="" />
      &#x3C;HeaderAlignment Value="" />
      &#x3C;AutoSizeMode Value="" />
      &#x3C;HeaderBackColor>&#x3C;/HeaderBackColor>
      &#x3C;BackColor>&#x3C;/BackColor>
      &#x3C;ForeColor>&#x3C;/ForeColor>
      &#x3C;Visible>&#x3C;/Visible>
      &#x3C;Hint>&#x3C;/Hint>
      &#x3C;DataType DataType="" />
      &#x3C;Substitution SourceColumn="">
        &#x3C;DataConnection SourceDataConnection="">
          &#x3C;Fields>
            &#x3C;Field Name="" />
            &#x3C;Field Name="" />
          &#x3C;/Fields>
        &#x3C;/DataConnection>
      &#x3C;/Substitution>
      &#x3C;Sorting>
        &#x3C;SortOrder Type="" />
        &#x3C;ColumnOrder Order="" />
      &#x3C;/Sorting>
      &#x3C;Filter AutoFill="" FilterNullValue="">&#x3C;/Filter>
      &#x3C;DefaultNewRowValue>&#x3C;/DefaultNewRowValue>
      &#x3C;AutoFill Type="" />
      &#x3C;Calculate>
        &#x3C;Expression>&#x3C;/Expression>
        &#x3C;Items>
          &#x3C;Item>&#x3C;/Item>
          &#x3C;Item>&#x3C;/Item>
        &#x3C;/Items>
      &#x3C;/Calculate>
      &#x3C;Format Value="" />
      &#x3C;NullValue Show="" />
      &#x3C;ManagementMode>&#x3C;/ManagementMode>
    &#x3C;/Column>
    &#x3C;Column Name="" Type="DatabaseTableColumnNumericBox" Assembly="DatabaseTableColumnControls" >
      &#x3C;Title>&#x3C;/Title>
      &#x3C;Width>&#x3C;/Width>
      &#x3C;DisplayIndex>&#x3C;/DisplayIndex>
      &#x3C;Frozen Value="" />
      &#x3C;WrapMode Value="" />
      &#x3C;ReadOnly>&#x3C;/ReadOnly> 
      &#x3C;AllowSort Value="" />
      &#x3C;Alignment Value="" />
      &#x3C;HeaderAlignment Value="" />
      &#x3C;AutoSizeMode Value="" />
      &#x3C;HeaderBackColor>&#x3C;/HeaderBackColor>
      &#x3C;BackColor>&#x3C;/BackColor>
      &#x3C;ForeColor>&#x3C;/ForeColor>
      &#x3C;Visible>&#x3C;/Visible>
      &#x3C;Hint>&#x3C;/Hint>
      &#x3C;DataType DataType="" />
      &#x3C;Substitution SourceColumn="">
        &#x3C;DataConnection SourceDataConnection="">
          &#x3C;Fields>
            &#x3C;Field Name="" />
            &#x3C;Field Name="" />
          &#x3C;/Fields>
        &#x3C;/DataConnection>
      &#x3C;/Substitution>
      &#x3C;Sorting>
        &#x3C;SortOrder Type="" />
        &#x3C;ColumnOrder Order="" />
      &#x3C;/Sorting>
      &#x3C;Filter AutoFill="" FilterNullValue="">&#x3C;/Filter>
      &#x3C;DefaultNewRowValue>&#x3C;/DefaultNewRowValue>
      &#x3C;AutoFill Type="" />
      &#x3C;Calculate>
        &#x3C;Expression>&#x3C;/Expression>
        &#x3C;Items>
          &#x3C;Item>&#x3C;/Item>
          &#x3C;Item>&#x3C;/Item>
        &#x3C;/Items>
      &#x3C;/Calculate>
      &#x3C;Increment Value="" />
      &#x3C;Maximum Value="" />
      &#x3C;Minimum Value="" />
      &#x3C;DecimalPlaces Value="" />
      &#x3C;ThousandsSeparator Value="" />
      &#x3C;ManagementMode>&#x3C;/ManagementMode>
    &#x3C;/Column>
  &#x3C;/Columns>
&#x3C;/MyObject>
</code></pre>

## Описание DatabaseTable <a href="#description" id="description"></a>

```xml
<MyObject Name="DatabaseTableName" Type="DatabaseTable" Assembly="ComplexControls">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для DatabaseTable-->
</MyObject>
```

DatabaseTable не имеет значения.

## Тэги, общие для всех графических объектов <a href="#common_tags" id="common_tags"></a>

### Width <a href="#width" id="width"></a>

Ширина таблицы.

Необязательный тэг. Ожидается целочисленное значение.

Если тэг `<Width>` отсутствует, то ширина таблицы определяется шириной всех ее видимых столбцов.

```xml
<Width>300</Width>
```

### ContextMenu <a href="#context_menu" id="context_menu"></a>

Контекстное меню объекта.

Необязательный тэг. Значение тэга `<ContextMenu>`: не ожидается.

```xml
<ContextMenu Name="ContextMenuName" MultiSelection="ContextMenuNameMultiSelection" />
```

#### Атрибуты тэга `<ContextMenu>` <a href="#attributes_tag_context_menu" id="attributes_tag_context_menu"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="477.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название контекстного меню для случая, когда выделена только одна строка в таблице.</p><p></p><p>Обязательный атрибут. Ожидается название одного из контекстных меню, описанных на форме.</p></td></tr><tr><td align="center">MultiSelection</td><td><p>Название контекстного меню для случая, когда выделено больше одной строки в таблице.</p><p></p><p>Необязательный атрибут. Ожидается название одного из контекстных меню, описанных на форме.</p></td></tr></tbody></table>

## Тэги, специфичные для DatabaseTable <a href="#specific-tags" id="specific-tags"></a>

### RowHeight <a href="#row_height" id="row_height"></a>

Высота строк с данными в таблице.

Необязательный тэг. Значение тэга `<RowHeight>`: не ожидается.

Если тэг `<RowHeight>` отсутствует, то для атрибута `Value` используется стандартное значение .NET.

```xml
<RowHeight Value="22" />
```

#### Атрибуты тэга `<RowHeight>` <a href="#attributes_tag_row_height" id="attributes_tag_row_height"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается целочисленное значение.</p></td></tr></tbody></table>

### ColumnHeadersHeight <a href="#column_headers_height" id="column_headers_height"></a>

Высота "шапки" таблицы.

Необязательный тэг. Значение тэга `<ColumnHeadersHeight>`: не ожидается.

Если тэг `<ColumnHeadersHeight>` отсутствует, то для атрибута `Value` используется стандартное значение .NET.

```xml
<ColumnHeadersHeight Value="21" />
```

#### Атрибуты тэга `<ColumnHeadersHeight>` <a href="#attributes_tag_column_headers_height" id="attributes_tag_column_headers_height"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается целочисленное значение.</p></td></tr></tbody></table>

### ColumnHeadersVisible <a href="#column_headers_visible" id="column_headers_visible"></a>

Признак, определяющий, показывать или нет "шапку" таблицы.

Необязательный тэг. Значение тэга `<ColumnHeadersVisible>`: не ожидается.

Если тэг `<ColumnHeadersVisible>` отсутствует, то для атрибута `Value` используется значение True.

```xml
<ColumnHeadersVisible Value="True" />
```

#### Атрибуты тэга `<ColumnHeadersVisible>` <a href="#attributes_tag_column_headers_visible" id="attributes_tag_column_headers_visible"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

### RowHeadersWidth <a href="#row_headers_width" id="row_headers_width"></a>

Ширина "нулевого" столбца таблицы.

Необязательный тэг. Значение тэга `<RowHeadersWidth>`: не ожидается.

Если тэг `<RowHeadersWidth>` отсутствует, то для атрибута `Value` используется стандартное значение .NET.

```xml
<RowHeadersWidth Value="40" />
```

#### Атрибуты тэга `<RowHeadersWidth>` <a href="#attributes_tag_row_headers_width" id="attributes_tag_row_headers_width"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается целочисленное значение.</p></td></tr></tbody></table>

### RowHeadersVisible <a href="#row_headers_visible" id="row_headers_visible"></a>

Признак, определяющий, показывать или нет "нулевой" столбец таблицы.

Необязательный тэг. Значение тэга `<RowHeadersVisible>`: не ожидается.

Если тэг `<RowHeadersVisible>` отсутствует, то для атрибута `Value` используется значение False.

```xml
<RowHeadersVisible Value="False" />
```

#### Атрибуты тэга `<RowHeadersVisible>` <a href="#attributes_tag_row_headers_visible" id="attributes_tag_row_headers_visible"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

### BackgroundColor <a href="#background_color" id="background_color"></a>

Цвет фона таблицы.

Необязательный тэг. Значение тэга `<BackgroundColor>`: не ожидается.

Если тэг `<BackgroundColor>` отсутствует, то для атрибута `Value` используется стандартное значение .NET.

```xml
<BackgroundColor Value="BackgroundColor" />
```

#### Атрибуты тэга `<BackgroundColor>` <a href="#attributes_tag_background_color" id="attributes_tag_background_color"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).</p></td></tr></tbody></table>

### BorderStyle <a href="#border_style" id="border_style"></a>

Название типа границ таблицы.

Необязательный тэг. Значение тэга `<BorderStyle>`: не ожидается.

Если тэг `<BorderStyle>` отсутствует, то для атрибута `Value` используется значение FixedSingle.

```xml
<BorderStyle Value="FixedSingle" />
```

#### Атрибуты тэга `<BorderStyle>` <a href="#attributes_tag_border_style" id="attributes_tag_border_style"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается название одного из <a href="./#border_style_types">типов границ таблицы</a>.</p></td></tr></tbody></table>

#### Типы границ таблицы <a href="#border_style_types" id="border_style_types"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="460.3333333333333"></th></tr></thead><tbody><tr><td align="center">None</td><td>Нет границ</td></tr><tr><td align="center">FixedSingle</td><td>Одиночная плоская</td></tr><tr><td align="center">Fixed3D</td><td>Одиночная объемная</td></tr></tbody></table>

### CellBorderStyle <a href="#cell_border_style" id="cell_border_style"></a>

Название стиля границ ячеек в таблице.

Необязательный тэг. Значение тэга `<CellBorderStyle>`: не ожидается.

Если тэг `<CellBorderStyle>` отсутствует, то для атрибута `Value` используется значение Single.

```xml
<CellBorderStyle Value="Single" />
```

#### Атрибуты тэга `<CellBorderStyle>` <a href="#attributes_tag_cell_border_style" id="attributes_tag_cell_border_style"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается название одного из <a href="./#cell_border_style_types">стилей границ ячеек</a> в таблице.</p></td></tr></tbody></table>

#### Стили границ ячеек <a href="#cell_border_style_types" id="cell_border_style_types"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="460.3333333333333"></th></tr></thead><tbody><tr><td align="center">Custom</td><td>Граница, которая была настроена</td></tr><tr><td align="center">Single</td><td>Одинарная граница</td></tr><tr><td align="center">Raised</td><td>Трехмерная выпуклая граница</td></tr><tr><td align="center">Sunken</td><td>Трехмерная утопленная граница</td></tr><tr><td align="center">None</td><td>Отсутствие границ</td></tr><tr><td align="center">SingleVertical</td><td>Вертикальная одинарная граница</td></tr><tr><td align="center">RaisedVertical</td><td>Вертикальная трехмерная выпуклая граница</td></tr><tr><td align="center">SunkenVertical</td><td>Вертикальная трехмерная утопленная граница</td></tr><tr><td align="center">SingleHorizontal</td><td>Горизонтальная одинарная граница</td></tr><tr><td align="center">RaisedHorizontal</td><td>Горизонтальная трехмерная выпуклая граница</td></tr><tr><td align="center">SunkenHorizontal</td><td>Горизонтальная трехмерная утопленная граница</td></tr></tbody></table>

### HideSelection <a href="#hide_selection" id="hide_selection"></a>

Признак видимости выделения в таблице.

Необязательный тэг. Значение тэга `<HideSelection>`: не ожидается.

Если тэг `<HideSelection>` отсутствует, то для атрибута `Value` используется значение False.

```xml
<HideSelection Value="False" />
```

#### Атрибуты тэга `<HideSelection>` <a href="#attributes_tag_hide_selection" id="attributes_tag_hide_selection"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

Замечание. Невидимость выделения задается посредством присвоения внутренним свойствам `<SelectionForeColor>` и `<SelectionBackColor>` значений из свойств `<ForeColor>` и `<BackColor>`, либо при задании значения True для set-проперти HideSelection.

### SelectionColor <a href="#selection_color" id="selection_color"></a>

Настройки цвета выделения в таблице.

Необязательный тэг. Значение тэга `<SelectionColor>`: не ожидается.

Если тэг `<SelectionColor>` отсутствует, то используется системный цвет выделения.

```xml
<SelectionColor Name="LightBlue" FadingRatio="0.55" />
```

#### Атрибуты тэга `<SelectionColor>` <a href="#attributes_tag_selection_color" id="attributes_tag_selection_color"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Имя цвета или описание цвета в формате HTML (#rrggbb).</p><p></p><p>Обязательный атрибут. Ожидается имя одного из цветов, описанных на форме.</p></td></tr><tr><td align="center">FadingRatio</td><td><p>Степень остатка цвета фона при выделении (0 - минимальный остаток, выделенная строка полностью закрашена цветом; 1 - минимальный остаток, выделенная строка не закрашена вовсе).</p><p></p><p>Необязательный атрибут. Ожидается числовое значение от 0 до 1.</p><p></p><p>Если атрибут <code>FadingRatio</code> не задан, то используется значение 0,55.</p></td></tr></tbody></table>

### AllowInsert <a href="#allow_insert" id="allow_insert"></a>

Признак, определяющий, может ли пользователь добавлять строки в таблицу посредством графического интерфейса таблицы.

Необязательный тэг. Ожидается логическое значение.

Если тэг `<AllowInsert>` отсутствует, то используется значение True.

```xml
<AllowInsert>True</AllowInsert>
```

### AllowUpdate <a href="#allow_update" id="allow_update"></a>

Признак, определяющий, может ли пользователь изменять значения в строках таблицы посредством графического интерфейса таблицы.

Необязательный тэг. Ожидается логическое значение.

Если тэг `<AllowUpdate>` отсутствует, то используется значение True.

```xml
<AllowUpdate>True</AllowUpdate>
```

### AllowDelete <a href="#allow_delete" id="allow_delete"></a>

Признак, определяющий, может ли пользователь удалять строки из таблицы посредством графического интерфейса таблицы.

Необязательный тэг. Ожидается логическое значение.

Если тэг `<AllowDelete>` отсутствует, то используется значение True.

```xml
<AllowDelete>True</AllowDelete>
```

### MultiSelect <a href="#multi_select" id="multi_select"></a>

Признак, определяющий, можно ли выделить в таблице более одной строки одновременно.

Необязательный тэг. Значение тэга `<MultiSelect>`: не ожидается.

Если тэг `<MultiSelect>` отсутствует, то для атрибута `Value` используется значение False.

```xml
<MultiSelect Value="False" />
```

#### Атрибуты тэга `<MultiSelect>` <a href="#attributes_tag_multi_select" id="attributes_tag_multi_select"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

### ScrollBars <a href="#scroll_bars" id="scroll_bars"></a>

Признак, определяющий, тип полос прокрутки в таблице.

Необязательный тэг. Значение тэга `<ScrollBars>`: не ожидается.

Если тэг `<ScrollBars>` отсутствует, то для атрибута `Value` используется значение Both.

```xml
<ScrollBars Value="None" />
```

#### Атрибуты тэга `<ScrollBars>` <a href="#attributes_tag_scroll_bars" id="attributes_tag_scroll_bars"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается название одного из <a href="./#scroll_bars_types">типов полос прокрутки</a> в таблице.</p></td></tr></tbody></table>

#### Типы полос прокрутки <a href="#scroll_bars_types" id="scroll_bars_types"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="460.3333333333333"></th></tr></thead><tbody><tr><td align="center">Both</td><td>Разрешены вертикальная и горизонтальная полосы прокрутки</td></tr><tr><td align="center">Vertical</td><td>Только вертикальная полоса прокрутки</td></tr><tr><td align="center">Horizontal</td><td>Только горизонтальная полоса прокрутки</td></tr><tr><td align="center">None</td><td>Нет полос прокрутки</td></tr></tbody></table>

### SelectionMode <a href="#selection_mode" id="selection_mode"></a>

Название типа выделения таблицы.

Необязательный тэг. Значение тэга `<SelectionMode>`: не ожидается.

Если тэг `<SelectionMode>` отсутствует, то для атрибута Value используется значение FullRowSelect.

```xml
<SelectionMode Value="RowHeaderSelect" />
```

#### Атрибуты тэга `<SelectionMode>` <a href="#attributes_tag_selection_mode" id="attributes_tag_selection_mode"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается название одного из <a href="./#selection_mode_types">типов выделения таблицы</a>.</p></td></tr></tbody></table>

#### Типы выделения таблицы <a href="#selection_mode_types" id="selection_mode_types"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="460.3333333333333"></th></tr></thead><tbody><tr><td align="center">CellSelect</td><td>Выделение ячеек по отдельности</td></tr><tr><td align="center">FullRowSelect</td><td>Выделение всей строки сразу</td></tr><tr><td align="center">FullColumnSelect</td><td>Выделение всего столбца сразу (возможно применить только, если в таблице нет столбцов с характеристикой SortMode, имеющей значение True)</td></tr><tr><td align="center">RowHeaderSelect</td><td>Выделение ячеек по отдельности с возможностью выделить сразу всю строку)</td></tr><tr><td align="center">ColumnHeaderSelect</td><td>Выделение ячеек по отдельности с возможностью выделить сразу весь столбец)</td></tr></tbody></table>

### BeginEditOnCellEnter <a href="#begin_edit_on_cell_enter" id="begin_edit_on_cell_enter"></a>

Признак, определяющий, будет ли выделенная ячейка автоматически переводится в режим редактирования.

Необязательный тэг. Значение тэга не ожидается.

По умолчанию для атрибута `Value` используется значение False.

```xml
<BeginEditOnCellEnter Value="True" />
```

### EditMode <a href="#edit_mode" id="edit_mode"></a>

Название типа редактирования ячеек таблицы.

Необязательный тэг. Значение тэга не ожидается.

```xml
<EditMode Value="EditOnKeystrokeOrF2" />
```

В атрибуте `Value` ожидается название одного из типов редактирования ячеек таблицы:

<table data-header-hidden><thead><tr><th width="231.55224634023222" align="center"></th><th width="460.3333333333333"></th></tr></thead><tbody><tr><td align="center">CellSelectEditOnEnter</td><td>Редактирование начинается, когда ячейка получает фокус</td></tr><tr><td align="center">EditOnF2</td><td>Редактирование начинается при нажатии на кнопку F2, когда ячейка имеет фокус</td></tr><tr><td align="center">EditOnKeystroke</td><td>Редактирование начинается при нажатии на любую букво-цифровую кнопку, когда ячейка имеет фокус</td></tr><tr><td align="center">EditOnKeystrokeOrF2</td><td>Редактирование начинается при нажатии на кнопку F2 или на любую букво-цифровую кнопку, когда ячейка имеет фокус</td></tr><tr><td align="center">EditProgrammatically</td><td>Редактирование через графический интерфейс таблицы запрещено</td></tr></tbody></table>

По умолчанию для атрибута `Value` используется значение EditOnKeystrokeOrF2.

### AllowResizeColumns <a href="#allow_resize_columns" id="allow_resize_columns"></a>

Признак, определяющий, может ли пользователь изменять ширину столбцов посредством графического интерфейса таблицы.

Необязательный тэг. Значение тэга `<AllowResizeColumns>`: не ожидается.

Если тэг `<AllowResizeColumns>` отсутствует, то для атрибута `Value` используется значение True.

```xml
<AllowResizeColumns Value="True" />
```

#### Атрибуты тэга `<AllowResizeColumns>` <a href="#attributes_tag_allow_resize_columns" id="attributes_tag_allow_resize_columns"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

### AllowOrderColumns <a href="#allow_order_columns" id="allow_order_columns"></a>

Признак, определяющий, может ли пользователь изменять порядок отображения столбцов посредством графического интерфейса таблицы.

Необязательный тэг. Значение тэга `<AllowOrderColumns>`: не ожидается.

Если тэг `<AllowOrderColumns>` отсутствует, то для атрибута `Value` используется значение False.

```xml
<AllowOrderColumns Value="False" />
```

#### Атрибуты тэга `<AllowOrderColumns>` <a href="#attributes_tag_allow_order_columns" id="attributes_tag_allow_order_columns"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

### AllowResizeRows <a href="#allow_resize_rows" id="allow_resize_rows"></a>

Признак, определяющий, может ли пользователь изменять высоту строк посредством графического интерфейса таблицы.

Необязательный тэг. Значение тэга `<AllowResizeRows>`: не ожидается.

Если тэг `<AllowResizeRows>` отсутствует, то для атрибута `Value` используется значение True.

```xml
<AllowResizeRows Value="True" />
```

#### Атрибуты тэга `<AllowResizeRows>` <a href="#attributes_tag_allow_resize_rows" id="attributes_tag_allow_resize_rows"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

### AutoSizeRowsMode <a href="#auto_size_rows_mode" id="auto_size_rows_mode"></a>

Название типа автоматического изменения высоты строк таблицы.

Необязательный тэг. Значение тэга `<AutoSizeRowsMode>`: не ожидается.

Если тэг `<AutoSizeRowsMode>` отсутствует, то для атрибута `Value` используется значение None.

```xml
<AutoSizeRowsMode Value="None" />
```

#### Атрибуты тэга `<AutoSizeRowsMode>` <a href="#attributes_tag_auto_size_rows_mode" id="attributes_tag_auto_size_rows_mode"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается название одного из <a href="./#auto_size_rows_mode_types">типов автоматического изменения высоты строк таблицы</a>.</p></td></tr></tbody></table>

#### Типы автоматического изменения высоты строк таблицы <a href="#auto_size_rows_mode_types" id="auto_size_rows_mode_types"></a>

<table data-header-hidden><thead><tr><th width="286.33197012750384" align="center"></th><th width="460.3333333333333"></th></tr></thead><tbody><tr><td align="center">None</td><td>Нет автоматического изменения высоты строк таблицы</td></tr><tr><td align="center">AllCells</td><td>Высота строк изменяется в соответствии с содержимым всех ячеек в строках, включая ячейки заголовка</td></tr><tr><td align="center">AllCellsExceptHeaders</td><td>Высота строк изменяется в соответствии с содержимым всех ячеек в строках, исключая ячейки заголовка</td></tr><tr><td align="center">AllHeaders</td><td>Высота строк изменяется в соответствии с содержимым заголовка строк</td></tr><tr><td align="center">DisplayedCells</td><td>Высота строк изменяется в соответствии с содержимым всех ячеек в строках, отображаемых в текущий момент на экране, включая ячейки заголовка</td></tr><tr><td align="center">DisplayedCellsExceptHeaders</td><td>Высота строк изменяется в соответствии с содержимым всех ячеек в строках, отображаемых в текущий момент на экране, исключая ячейки заголовка</td></tr><tr><td align="center">DisplayedHeaders</td><td>Высота строк изменяется в соответствии с содержимым заголовков строк, отображаемых в текущий момент на экране</td></tr></tbody></table>

### AutoSizeColumnsMode <a href="#auto_size_columns_mode" id="auto_size_columns_mode"></a>

Название типа автоматического изменения ширины столбцов таблицы.

Необязательный тэг. Значение тэга `<AutoSizeColumnsMode>`: не ожидается.

Если тэг `<AutoSizeColumnsMode>` отсутствует, то для атрибута `Value` используется значение None.

```xml
<AutoSizeColumnsMode Value="None" />
```

#### Атрибуты тэга `<AutoSizeColumnsMode>` <a href="#attributes_tag_auto_size_columns_mode" id="attributes_tag_auto_size_columns_mode"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается название одного из <a href="./#auto_size_columns_mode_types">типов автоматического изменения ширины столбцов таблицы</a>.</p></td></tr></tbody></table>

#### Типы автоматического изменения ширины столбцов таблицы <a href="#auto_size_columns_mode_types" id="auto_size_columns_mode_types"></a>

<table data-header-hidden><thead><tr><th width="286.33197012750384" align="center"></th><th width="460.3333333333333"></th></tr></thead><tbody><tr><td align="center">None</td><td>Пропорциональное автоматическое изменение ширины столбцов относительно ширины таблицы</td></tr><tr><td align="center">AllCells</td><td>Ширина столбцов изменяется в соответствии с содержимым всех ячеек в столбцах, включая ячейки заголовка</td></tr><tr><td align="center">AllCellsExceptHeader</td><td>Ширина столбцов изменяется в соответствии с содержимым всех ячеек в столбцах, исключая ячейки заголовка</td></tr><tr><td align="center">ColumnHeader</td><td>Ширина столбцов изменяется в соответствии с содержимым заголовка столбцов</td></tr><tr><td align="center">DisplayedCells</td><td>Ширина столбцов изменяется в соответствии с содержимым всех ячеек в столбцах, отображаемых в текущий момент на экране, включая ячейки заголовка</td></tr><tr><td align="center">DisplayedCellsExceptHeaders</td><td>Ширина столбцов изменяется в соответствии с содержимым всех ячеек в столбцах, отображаемых в текущий момент на экране, исключая ячейки заголовка</td></tr><tr><td align="center">Fill</td><td>Ширина столбцов изменяется так, чтобы точно заполнить ширину всей отображаемой области таблицы, с учетом наличия или отсутствия полосы горизонтальной прокрутки</td></tr><tr><td align="center">Disable</td><td>Нет автоматического изменения ширины столбцов таблицы</td></tr></tbody></table>

### AllowFilterColumns <a href="#allow_filter_columns" id="allow_filter_columns"></a>

Признак, определяющий, может ли пользователь фильтровать таблицу.

Необязательный тэг. Значение тэга `<AllowFilterColumns>`: не ожидается.

Если тэг `<AllowFilterColumns>` отсутствует, то для атрибута `Value` используется значение True.

```xml
<AllowFilterColumns Value="False" />
```

#### Атрибуты тэга `<AllowFilterColumns>` <a href="#attributes_tag_allow_filter_columns" id="attributes_tag_allow_filter_columns"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

### ColumnHeadersHeightSizeMode <a href="#column_headers_height_size_mode" id="column_headers_height_size_mode"></a>

Название типа возможности изменения высоты шапки таблицы.

Необязательный тэг. Значение тэга `<ColumnHeadersHeightSizeMode>`: не ожидается.

Если тэг `<ColumnHeadersHeightSizeMode>` отсутствует, то для атрибута `Value` используется значение DisableResizing.

```xml
<ColumnHeadersHeightSizeMode Value="DisableResizing" />
```

#### Атрибуты тэга `<ColumnHeadersHeightSizeMode>` <a href="#attributes_tag_column_headers_height_size_mode" id="attributes_tag_column_headers_height_size_mode"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается название одного из <a href="./#column_headers_height_size_mode_types">типов возможности изменения высоты шапки таблицы</a>.</p></td></tr></tbody></table>

#### Типы возможности изменения высоты шапки таблицы <a href="#column_headers_height_size_mode_types" id="column_headers_height_size_mode_types"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">AutoSize</td><td>Автоматическая высота шапки таблицы</td></tr><tr><td align="center">EnableResizing</td><td>Возможность изменения высоты шапки таблицы</td></tr><tr><td align="center">DisableResizing</td><td>Запрет на изменения высоты шапки таблицы</td></tr></tbody></table>

### ColumnHeadersAlignment <a href="#column_headers_alignment" id="column_headers_alignment"></a>

Название типа положения содержимого заголовка столбца таблицы.

Необязательный тэг. Значение тэга `<ColumnHeadersAlignment>`: не ожидается.

Если тэг `<ColumnHeadersAlignment>` отсутствует, то для атрибута `Value` используется значение NotSet.

```xml
<ColumnHeadersAlignment Value="NotSet" />
```

#### Атрибуты тэга `<ColumnHeadersAlignment>` <a href="#attributes_tag_column_headers_alignment" id="attributes_tag_column_headers_alignment"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается название одного из <a href="./#column_headers_alignment_types">типов положения содержимого ячейки столбца таблицы</a>.</p></td></tr></tbody></table>

#### Типы положения содержимого ячейки столбца таблицы <a href="#column_headers_alignment_types" id="column_headers_alignment_types"></a>

<table data-header-hidden><thead><tr><th width="286.33197012750384" align="center"></th><th width="460.3333333333333"></th></tr></thead><tbody><tr><td align="center">NotSet</td><td>Не установлено</td></tr><tr><td align="center">TopLeft</td><td>Содержимое выравнивается по верхнему краю в вертикальном направлении и по левому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">TopCenter</td><td>Содержимое выравнивается по верхнему краю в вертикальном направлении и по центру ячейки</td></tr><tr><td align="center">TopRight</td><td>Содержимое выравнивается по верхнему краю в вертикальном направлении и по правому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">MiddleLeft</td><td>Содержимое выравнивается вертикально по середине и горизонтально по левому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">MiddleCenter</td><td>Содержимое выравнивается по вертикальному и горизонтальному центру ячейки</td></tr><tr><td align="center">MiddleRight</td><td>Содержимое выравнивается вертикально по середине и горизонтально по правому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">BottomLeft</td><td>Содержимое выравнивается по нижнему краю в вертикальном направлении и по левому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">BottomCenter</td><td>Содержимое выравнивается по нижнему краю в вертикальном направлении и по центру ячейки</td></tr><tr><td align="center">BottomRight</td><td>Содержимое выравнивается по нижнему краю в вертикальном направлении и по правому краю ячейки в горизонтальном направлении</td></tr></tbody></table>

### ShowCellHints <a href="#show_cell_hints" id="show_cell_hints"></a>

Признак, определяющий, будут ли показываться всплывающие подсказки для ячеек таблицы.

Необязательный тэг. Значение тэга не ожидается.

По умолчанию используется значение False.

```xml
<ShowCellHints Value="True" />
```

#### трибуты тэга `<ShowCellHints>` <a href="#attributes_tag_show_cell_hints" id="attributes_tag_show_cell_hints"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

### ColumnContextMenuBackColor <a href="#column_context_menu_back_color" id="column_context_menu_back_color"></a>

Цвет фона контекстного меню фильтрации и сортировки.

Необязательный тэг. Значение тэга не ожидается.

По умолчанию используется стандартное значение.

```xml
<ColumnContextMenuBackColor Name="Green" />
```

#### Атрибуты тэга `<ColumnContextMenuBackColor>` <a href="#attributes_tag_column_context_menu_fore_color" id="attributes_tag_column_context_menu_fore_color"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название цвета.</p><p></p><p>Обязательный атрибут. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).</p></td></tr></tbody></table>

### ColumnContextMenuForeColor <a href="#column_context_menu_fore_color" id="column_context_menu_fore_color"></a>

Цвет шрифта контекстного меню фильтрации и сортировки.

Необязательный тэг. Значение тэга не ожидается.

По умолчанию используется стандартное значение.

```xml
<ColumnContextMenuForeColor Name="Red" />
```

#### Атрибуты тэга `<ColumnContextMenuForeColor>` <a href="#attributes_tag_column_context_menu_fore_color" id="attributes_tag_column_context_menu_fore_color"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название цвета.</p><p></p><p>Обязательный атрибут. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).</p></td></tr></tbody></table>

### ColumnContextMenuWiden <a href="#column_context_menu_widen" id="column_context_menu_widen"></a>

Признак, определяющий, будет ли системное контекстное меню шире.

Необязательный тег. Значение тэга не ожидается.

Обязательный атрибут `Value` ожидает логическое значение. По умолчанию используется значение False.

```xml
<ColumnContextMenuWiden Value="True" />
```

### ShowExportToExcel <a href="#show_export_to_excel" id="show_export_to_excel"></a>

Признак, определяющий, будет ли показываться элемент контекстного меню "Выгрузить в Excel".

Необязательный тэг. Значение тэга не ожидается.

Необязательный атрибут `Value` ожидает логическое значение. По умолчанию используется значение True.

```xml
<ShowExportToExcel Value="False" />
```

### Formatting <a href="#formatting" id="formatting"></a>

Условное форматирование ячеек таблицы на основе значений других ячеек таблицы в этой же строке.

Необязательный тэг. Значение тэга [`<Formatting>`](formatting/): список тэгов [`<BackColor>`](formatting/back_color.md), [`<ForeColor>`](formatting/fore_color.md), [`<FontStyle>`](formatting/font_style.md) и [`<Alignment>`](formatting/alignment.md).

```xml
<Formatting>
  <BackColor Name="BackColor">
    <Columns>
      <Column Name="ColumnName1" />
      <Column Name="ColumnName2" />
    </Columns>
    <Expression>ColumnName3 > {0} * {1}</Expression>
    <Items>
      <Item>10</Item>
      <Item>20</Item>
    </Items>
  </BackColor>
  <ForeColor Name="ForeColor">
    <Columns>
      <Column Name="ColumnName1" />
      <Column Name="ColumnName2" />
    </Columns>
    <Expression>ColumnName3 > {0} * {1}</Expression>
    <Items>
      <Item>10</Item>
      <Item>20</Item>
    </Items>
  </ForeColor>
  <FontStyle Name="FontStyle">
    <Columns>
      <Column Name="ColumnName1" />
      <Column Name="ColumnName2" />
    </Columns>
    <Expression>ColumnName3 > {0} * {1}</Expression>
    <Items>
      <Item>10</Item>
      <Item>20</Item>
    </Items>
  </FontStyle>
  <Alignment>
    <Value>MiddleCenter</Value>
    <Columns>
      <Column Name="ColumnName1" />
    </Columns>
    <Expression>ColumnName3 > {0}</Expression>
    <Items>
      <Item>10</Item>
    </Items>
  </Alignment>
  <Alignment Value="MiddleRight">
    <Columns>
      <Column Name="ColumnName2" />
    </Columns>
    <Expression>ColumnName4</Expression>
  </Alignment>
</Formatting>
```

### SourceDataConnection <a href="#source_data_connection" id="source_data_connection"></a>

Загружающее соединение с данными, данные которого будут размещены в таблице.&#x20;

Необязательный тэг. Значение тэга `<SourceDataConnection>`: не ожидается.

```xml
<SourceDataConnection Name="SourceDataConnection" Query="QueryName"/>
```

#### Атрибуты тэга `<SourceDataConnection>` <a href="#attributes_tag_source_data_connection" id="attributes_tag_source_data_connection"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается имя одного из загружающих соединений с данными, описанных на форме.</p></td></tr><tr><td align="center">Query</td><td><p>Значение.</p><p></p><p>Необязательный атрибут. Ожидается имя одного из запросов загружающего соединения с данными, описанных на форме.</p></td></tr></tbody></table>

### SaveOnFormClose <a href="#save_on_form_close" id="save_on_form_close"></a>

Настройки сохранения информации о таблице. Признак, определяющий, будет ли сохранена информация о таблице.

Необязательный тэг. Значение тэга `<SaveOnFormClose>`: не ожидается.

Если тэг `<SaveOnFormClose>` отсутствует, то для атрибутов `Columns`, `Filter` и `Sort` используются значения False, False, и False соответственно.

```xml
<SaveOnFormClose Columns="True" Filter="True" Sort="True" />
```

#### Атрибуты тэга `<SaveOnFormClose>` <a href="#attributes_tag_save_on_form_close" id="attributes_tag_save_on_form_close"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Columns</td><td><p>Признак, определяющий, будет ли сохраняться информация о ширине, порядке, видимости столбцов таблицы. Для того, чтобы сохранить ширину столбцов у столбца в тэге <a href="./#column_auto_size_mode"><code>&#x3C;AutoSizeMode></code></a> в атрибуте <code>Value</code> должно быть указано значение None.</p><p></p><p>Необязательный атрибут. Ожидается логическое значение. </p></td></tr><tr><td align="center">Filter</td><td><p>Признак, определяющий, будут ли сохраняться фильтры в таблице.</p><p></p><p>Необязательный атрибут. Ожидается логическое значение. </p></td></tr><tr><td align="center">Sort</td><td><p>Признак, определяющий, будут ли сохраняться сортировки в таблице.</p><p></p><p>Необязательный атрибут. Ожидается логическое значение. </p></td></tr></tbody></table>

### Columns <a href="#columns" id="columns"></a>

Список столбцов таблицы.

Обязательный тэг. Ожидается список тэгов [`<Column>`](column/), содержащих описание столбцов.

```xml
<Columns>
  <Column Name="ColumnName1" Type="DatabaseTableColumnTextBox" Assembly="DatabaseTableColumnControls">
    <!--Тэги, общие для всех столбцов таблицы-->
    <Title></Title>
    <Width></Width>
    <Visible></Visible>
    <ManagementMode></ManagementMode>
    <MinimumWidth></MinimumWidth>
    <ToolTipColumnName />
  </Column>
  <Column Name="ColumnName2" Type="DatabaseTableColumnComboBox" Assembly="DatabaseTableColumnControls">
    <!--Тэги, общие для всех столбцов таблицы-->
    <Title></Title>
    <Width></Width>
    <Visible></Visible>
    <ManagementMode></ManagementMode>
    <MinimumWidth></MinimumWidth>
    <ToolTipColumnName />
    <!--Тэги, специфичные для данного типа столбца-->
    <ValueList></ValueList>
  </Column>
  <Column Name="" Type="DatabaseTableColumnCheckBox" Assembly="DatabaseTableColumnControls">
    <!--Тэги, общие для всех столбцов таблицы-->
    <Title></Title>
    <Width></Width>
    <Visible></Visible>
    <ManagementMode></ManagementMode>
    <MinimumWidth></MinimumWidth>
    <ToolTipColumnName />
    <!--Тэги, специфичные для данного типа столбца-->
    <ThreeState Value="True" />
    <HeaderCheckAll Value="True" />
  </Column>
  <Column Name="ColumnName4" Type="DatabaseTableColumnDateTimePicker" Assembly="DatabaseTableColumnControls">
    <!--Тэги, общие для всех столбцов таблицы-->
    <Title></Title>
    <Width></Width>
    <Visible></Visible>
    <ManagementMode></ManagementMode>
    <MinimumWidth></MinimumWidth>
    <ToolTipColumnName />
    <!--Тэги, специфичные для данного типа столбца-->
    <Format Value="" />
    <NullValue Show="False" />
    <ShowCalendar Value="False" />
  </Column>
  <Column Name="ColumnName5" Type="DatabaseTableColumnNumericBox" Assembly="DatabaseTableColumnControls">
    <!--Тэги, общие для всех столбцов таблицы-->
    <Title></Title>
    <Width></Width>
    <Visible></Visible>
    <ManagementMode></ManagementMode>
    <MinimumWidth></MinimumWidth>
    <ToolTipColumnName />
    <!--Тэги, специфичные для данного типа столбца-->
    <Maximum Value="100" />
    <Increment Value="1" />
  </Column>
</Columns>
```

#### Атрибуты столбцов DatabaseTable <a href="#attributes_columns" id="attributes_columns"></a>

<table data-header-hidden><thead><tr><th width="158.6296484971982" align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название столбца (обязательно должно совпадать с именем поля, указанным в соединении с данными из тэга <a href="./#source_data_connection"><code>&#x3C;SourceDataConnection></code></a>).</p><p></p><p>Обязательный атрибут.</p></td></tr><tr><td align="center">Type</td><td><p>Название типа столбца в сборке.</p><p></p><p>Обязательный атрибут.</p></td></tr><tr><td align="center">Assembly</td><td><p>Название сборки (библиотека).</p><p></p><p>Обязательный атрибут.</p></td></tr></tbody></table>

Колонки таблицы могут быть одно из доступных типов:

* [DatabaseTableColumnTextBox](column/column_text_box.md) - используется для отображения данных в виде текста;
* [DatabaseTableColumnComboBox](column/column_combo_box.md) - позволяет пользователям выбирать значение из выпадающего списка, если в таблице разрешено редактирование (тэг [`<AllowUpdate>`](./#allow_update) имеет значение True);
* [DatabaseTableColumnCheckBox](column/column_check_box.md) - используется для отображения столбцов логических данных в виде CheckBox;
* [DatabaseTableColumnDateTimePicker](column/column_date_time_picker.md) - используется для отображения дат и времени в заданном формате и предоставляет пользователю возможностью выбирать значение в раскрывающемся календаре, если в таблице разрешено редактирование (тэг `<AllowUpdate>` имеет значение True);
* [DatabaseTableColumnNumericBox](column/column_numeric_box.md) - используется для отображения числовых значений и предоставляет пользователю возможностью задавать значение через NumericBox, если в таблице разрешено редактирование (тэг `<AllowUpdate>` имеет значение True).

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### RowHeight <a href="#get_row_height" id="get_row_height"></a>

Возвращает высоту строк с данными в таблице.

```xml
<Object Name="DatabaseTableName">
  <Property Name="RowHeight" />
</Object>
```

### ColumnHeadersHeight <a href="#get_column_headers_height" id="get_column_headers_height"></a>

Возвращает высоту "шапки" таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="ColumnHeadersHeight" />
</Object>
```

### ColumnHeadersVisible <a href="#get_column_headers_visible" id="get_column_headers_visible"></a>

Возвращает признак, определяющий, показывать или нет "шапку" таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="ColumnHeadersVisible" />
</Object>
```

### RowHeadersWidth <a href="#get_row_headers_width" id="get_row_headers_width"></a>

Возвращает ширину "нулевого" столбца таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="RowHeadersWidth" />
</Object>
```

### RowHeadersVisible <a href="#get_row_headers_visible" id="get_row_headers_visible"></a>

Возвращает признак, определяющий, показывать или нет "нулевой" столбец таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="RowHeadersVisible" />
</Object>
```

### BackgroundColor <a href="#get_background_color" id="get_background_color"></a>

Возвращает имя цвета фона таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="BackgroundColor" />
</Object>
```

### BorderStyle <a href="#get_border_style" id="get_border_style"></a>

Возвращает название типа границ таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="BorderStyle" />
</Object>
```

### CellBorderStyle <a href="#get_cell_border_style" id="get_cell_border_style"></a>

Возвращает название стиля границ ячеек в таблице.

```xml
<Object Name="DatabaseTableName">
  <Property Name="CellBorderStyle" />
</Object>
```

### HideSelection <a href="#get_hide_selection" id="get_hide_selection"></a>

Возвращает признак видимости выделения в таблице.

```xml
<Object Name="DatabaseTableName">
  <Property Name="HideSelection" />
</Object>
```

### AllowInsert <a href="#get_allow_insert" id="get_allow_insert"></a>

Возвращает признак, определяющий, может ли пользователь добавлять строки в таблицу посредством графического интерфейса таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="AllowInsert" />
</Object>
```

### AllowUpdate <a href="#get_allow_update" id="get_allow_update"></a>

Возвращает признак, определяющий, может ли пользователь изменять значения в строках таблицы посредством графического интерфейса таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="AllowUpdate" />
</Object>
```

### AllowDelete <a href="#get_allow_delete" id="get_allow_delete"></a>

Возвращает признак, определяющий, может ли пользователь удалять строки из таблицы посредством графического интерфейса таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="AllowDelete" />
</Object>
```

### MultiSelect <a href="#get_multi_select" id="get_multi_select"></a>

Возвращает признак, определяющий, можно ли выделить в таблице более одной строки одновременно.

```xml
<Object Name="DatabaseTableName">
  <Property Name="MultiSelect" />
</Object>
```

### SelectionMode <a href="#get_selection_mode" id="get_selection_mode"></a>

Возвращает название типа выделения таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="SelectionMode" />
</Object>
```

### EditMode <a href="#get_edit_mode" id="get_edit_mode"></a>

Возвращает название типа редактирования ячеек таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="EditMode" />
</Object>
```

### AllowResizeColumns <a href="#get_allow_resize_columns" id="get_allow_resize_columns"></a>

Возвращает признак, определяющий, может ли пользователь изменять ширину столбцов посредством графического интерфейса таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="AllowResizeColumns" />
</Object>
```

### AllowOrderColumns <a href="#get_allow_order_columns" id="get_allow_order_columns"></a>

Возвращает признак, определяющий, может ли пользователь изменять порядок отображения столбцов посредством графического интерфейса таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="AllowOrderColumns" />
</Object>
```

### AllowResizeRows <a href="#get_allow_resize_rows" id="get_allow_resize_rows"></a>

Возвращает признак, определяющий, может ли пользователь изменять высоту строк посредством графического интерфейса таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="AllowResizeRows" />
</Object>
```

### AutoSizeRowsMode <a href="#get_auto_size_rows_mode" id="get_auto_size_rows_mode"></a>

Возвращает название типа автоматического изменения высот строк таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="AutoSizeRowsMode" />
</Object>
```

### Column <a href="#get_column" id="get_column"></a>

Возвращает линейный массив значений, содержащихся в определенном столбце таблицы.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="Column">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
    </Parameters>
  </Property>  
</Object>
```

### ColumnUniqueValues <a href="#get_column_unique_values" id="get_column_unique_values"></a>

Возвращает линейный массив уникальных значений, содержащихся в определенном столбце таблицы.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ColumnUniqueValues">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
    </Parameters>
  </Property>
</Object>
```

### ColumnTitle <a href="#get_column_title" id="get_column_title"></a>

Возвращает название столбца таблицы по имени столбца.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ColumnTitle">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
    </Parameters>
  </Property>
</Object>
```

### ColumnHint <a href="#get_column_hint" id="get_column_hint"></a>

Возвращает текст подсказки, всплывающей на заголовке столбца таблицы, по имени столбца.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ColumnHint">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
    </Parameters>
  </Property>
</Object>
```

### ColumnLeft <a href="#get_column_left" id="get_column_left"></a>

Возвращает координату по горизонтали для определенного столбца таблицы, относительно того объекта, где расположена таблица (без учёта полосы горизонтальной прокрутки).

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ColumnLeft">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
    </Parameters>
  </Property>
</Object>
```

### ColumnOffset <a href="#get_column_offset" id="get_column_offset"></a>

Возвращает координату по горизонтали для определенного столбца таблицы, относительно того объекта, где расположена таблица (с учётом положения полосы горизонтальной прокрутки).

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ColumnOffset">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
    </Parameters>
  </Property>
</Object>
```

### ColumnVisible <a href="#get_column_visible" id="get_column_visible"></a>

Возвращает видимость столбца.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ColumnVisible">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
    </Parameters>
  </Property>
</Object>
```

### ColumnDisplayIndex <a href="#get_column_display_index" id="get_column_display_index"></a>

Возвращает порядок отображения определенного столбца таблицы.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ColumnDisplayIndex">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
    </Parameters>
  </Property>
</Object>
```

### ColumnWidth <a href="#get_column_width" id="get_column_width"></a>

Возвращает ширину определенного столбца таблицы.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ColumnWidth">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
    </Parameters>
  </Property>
</Object>
```

### ColumnSum <a href="#get_column_sum" id="get_column_sum"></a>

Возвращает сумму значений всех ячеек в определенном столбце таблицы.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ColumnSum">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
    </Parameters>
  </Property>
</Object>
```

### ColumnHeaderCheckBoxState <a href="#get_column_header_check_box_state" id="get_column_header_check_box_state"></a>

Возвращает текущее состояние CheckBox в заголовке определенного столбца таблицы.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ColumnHeaderCheckBoxState">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
    </Parameters>
  </Property>
</Object>
```

### CountingSumMultiply <a href="#get_counting_sum_multiply" id="get_counting_sum_multiply"></a>

Возвращает сумму, состоящую из произведений значений ячеек из двух определенных столбцов.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="CountingSumMultiply">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName1: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName1">ColumnName1</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName2: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName2">ColumnName2</Parameter>
    </Parameters>
  </Property>
</Object>
```

### CountingSignSumMultiply <a href="#get_counting_sign_sum_multiply" id="get_counting_sign_sum_multiply"></a>

Возвращает сумму, состоящую из определенных произведений значений ячеек из двух определенных столбцов.

Признаком для включения произведения строки в общую сумму служит значение ячейки третьего столбца.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="CountingSignSumMultiply">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName1: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName1">ColumnName1</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName2: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName2">ColumnName2</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным SignColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="SignColumnName">SignColumnName</Parameter>
    </Parameters>
  </Property>
</Object>
```

### SelectedRowIndex <a href="#get_selected_row_index" id="get_selected_row_index"></a>

Возвращает номер первой выделенной строки таблицы.\
Если строка таблицы не выбрана, то get-проперти вернет значение -1.

```markup
<Object Name="DatabaseTableName">
  <Property Name="SelectedRowIndex" />
</Object>
```

### SelectedRowsIndices <a href="#get_selected_rows_indices" id="get_selected_rows_indices"></a>

Возвращает линейный массив индексов выделенных строк таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="SelectedRowsIndices" />
</Object>
```

### SelectedColumnName <a href="#get_selected_column_name" id="get_selected_column_name"></a>

Возвращает название столбца выделенной ячейки таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="SelectedColumnName" />
</Object>
```

### SelectedCellValue <a href="#get_selected_cell_value" id="get_selected_cell_value"></a>

Возвращает значение выделенной ячейки таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="SelectedCellValue" />
</Object>
```

### SelectedRowsCount <a href="#get_selected_rows_count" id="get_selected_rows_count"></a>

Возвращает количество выделенных строк в таблице.

```markup
<Object Name="DatabaseTableName">
  <Property Name="SelectedRowsCount" />
</Object>
```

### SelectedCellsSumByColumnName <a href="#get_selected_cells_sum_by_column_name" id="get_selected_cells_sum_by_column_name"></a>

Возвращает сумму значений выделенных ячеек в определенном столбце таблицы.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="SelectedCellsSumByColumnName">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
    </Parameters>
  </Property>
</Object>
```

### SelectedRowCellValueByColumnName <a href="#get_selected_row_cell_value_by_column_name" id="get_selected_row_cell_value_by_column_name"></a>

Возвращает значение ячейки определенного столбца выделенной строки таблицы.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="SelectedRowCellValueByColumnName">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
    </Parameters>
  </Property>
</Object>
```

### SelectedRowsCellValuesByColumnName <a href="#get_selected_rows_cell_values_by_column_name" id="get_selected_rows_cell_values_by_column_name"></a>

Возвращает линейный массив значений ячеек столбца ColumnName выделенных строк таблицы.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="SelectedRowsCellValuesByColumnName">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
    </Parameters>
  </Property>
</Object>
```

### RowsCount <a href="#get_rows_count" id="get_rows_count"></a>

Возвращает количество строк в таблице.

```xml
<Object Name="DatabaseTableName">
  <Property Name="RowsCount" />
</Object>
```

### RowIndexOf <a href="#get_row_index_of" id="get_row_index_of"></a>

Возвращает индекс строки, удовлетворяющей условиям соответствия названий столбцов и значений в этих столбцах.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="RowIndexOf">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnNames: ожидается линейный массив названий столбцов таблицы-->
      <Parameter Name="ColumnNames">
        <Structure Type="List">
          <Item>ColumnName1</Item>
          <Item>ColumnName2</Item>
        </Structure>
      </Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным Values: ожидается линейный массив любых значений-->
      <Parameter Name="Values">
        <Structure Type="List">
          <Item>Value1</Item>
          <Item>Value2</Item>
        </Structure>
      </Parameter>
    </Parameters>
  </Property>
</Object>
```

### RowsIndicesOf <a href="#get_rows_indices_of" id="get_rows_indices_of"></a>

Возвращает массив индексов строки, удовлетворяющих условиям соответствия названий столбцов и значений в этих столбцах.

При установке параметра SearchWithArrays поиск для каждого столбца будет вестись по значениям из переданного для него массива по такому принципу, чтобы очередное значение из таблицы совпадало хотя бы с одним значением из этого массива.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="RowsIndicesOf">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnNames: ожидается линейный массив названий столбцов таблицы-->
      <Parameter Name="ColumnNames">
        <Structure Type="List">
          <Item>ColumnName1</Item>
          <Item>ColumnName2</Item>
        </Structure>
      </Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным Values: ожидается линейный массив любых значений-->
      <!--При установленном параметре SearchWithArrays в качестве значения для каждого столбца допустимо передавать линейный массив любых значений, по которым и будет вестись поиск-->
      <Parameter Name="Values">
        <Structure Type="List">
          <Item>Value1</Item>
          <Item>
            <Structure Type="List">
              <Item>Value2</Item>
              <Item>Value3</Item>
            </Structure>
          </Item>
        </Structure>
      </Parameter>
      <!--Необязательный параметр. При отсутствии используется значение False-->
      <!--Значение тэга Parameter с атрибутом Name, равным SearchWithArrays: ожидается логическое значение-->
      <Parameter Name="SearchWithArrays">False</Parameter>
    </Parameters>
  </Property>
</Object>
```

### ValueByAnotherFieldValue <a href="#get_value_by_another_field_value" id="get_value_by_another_field_value"></a>

Возвращает значение ячейки одного столбца в строке, найденной по определенному значению другого столбца.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ValueByAnotherFieldValue">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным TargetField: ожидается название одного из столбцов таблицы-->
      <Parameter Name="TargetField">TargetColumnName</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным FilterValue: любое значение-->
      <Parameter Name="FilterValue">FilterValue</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным FilterField: ожидается название одного из столбцов таблицы-->
      <Parameter Name="FilterField">FilterColumnName</Parameter>
    </Parameters>
  </Property>
</Object>
```

### Data <a href="#get_data" id="get_data"></a>

Возвращает двумерную матрицу элементов с именованными столбцами, содержащую значения всех ячеек таблицы, удовлетворяющую выражению фильтра.

Все поддерживаемые в выражении фильтра конструкции смотрите по [ссылке](http://msdn.microsoft.com/en-us/library/system.data.datacolumn.expression.aspx).

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: любое значение-->
  <Property Name="Data">FilterField > 0</Property>
</Object>
```

### ArrayData <a href="#get_array_data" id="get_array_data"></a>

Возвращает двумерную матрицу элементов, содержащую значения всех ячеек таблицы.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: не ожидается-->
  <Property Name="ArrayData" />
</Object>
```

### DictionaryArrayData <a href="#get_dictionary_array_data" id="get_dictionary_array_data"></a>

Возвращает массив словарей, содержащих значения всех ячеек таблицы.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: не ожидается-->
  <Property Name="DictionaryArrayData" />
</Object>
```

### FilteredColumnValues <a href="#get_filtered_column_values" id="get_filtered_column_values"></a>

Возвращает массив элементов определенного столбца ColumnName, выбранных на основе выражения Filter, задающего фильтрацию строк таблицы.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="FilteredColumnValues">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: любое значение-->
      <!--Все поддерживаемые в выражении фильтра конструкции смотрите по ссылке "http://msdn.microsoft.com/en-us/library/system.data.datacolumn.expression.aspx"-->
      <Parameter Name="Filter">ColumnName > 1</Parameter>
    </Parameters>
  </Property>
</Object>
```

### RowAdded <a href="#get_row_added" id="get_row_added"></a>

Возвращает признак, была ли строка с определенным индексом сохранена в базе данных.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="RowAdded">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным Value: ожидается целочисленное значение-->
      <Parameter Name="Value">1</Parameter>
    </Parameters>
  </Property>
</Object>
```

### SortedColumn <a href="#get_sorted_column" id="get_sorted_column"></a>

Возвращает название столбца, по которому пользователь отсортировал таблицу.

```xml
<Object Name="DatabaseTableName">
  <Property Name="SortedColumn" />
</Object>
```

### SortDirection <a href="#get_sort_direction" id="get_sort_direction"></a>

Возвращает [направление сортировки столбца](./#sort_direction_types), по которому пользователь отсортировал таблицу.

```xml
<Object Name="DatabaseTableName">
  <Property Name="SortDirection" />
</Object>
```

#### Направления сортировки столбца <a href="#sort_direction_types" id="sort_direction_types"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="525.3333333333333"></th></tr></thead><tbody><tr><td align="center">ASC</td><td>По возрастанию</td></tr><tr><td align="center">DESC</td><td>По убыванию</td></tr><tr><td align="center">NULL</td><td>Нет пользовательской сортировки</td></tr></tbody></table>

### VerticalScrollOffset <a href="#get_vertical_scroll_offset" id="get_vertical_scroll_offset"></a>

Возвращает величину смещения полосы вертикальной прокрутки таблицы в пикселях.

```xml
<Object Name="DatabaseTableName">
  <Property Name="VerticalScrollOffset" />
</Object>
```

### HorizontalScrollOffset <a href="#get_horizontal_scroll_offset" id="get_horizontal_scroll_offset"></a>

Возвращает величину смещения полосы горизонтальной прокрутки таблицы в пикселях.

```xml
<Object Name="DatabaseTableName">
  <Property Name="HorizontalScrollOffset" />
</Object>
```

### LastCellClickedRowIndex <a href="#get_last_cell_clicked_row_index" id="get_last_cell_clicked_row_index"></a>

Возвращает индекс строки, по ячейке которой был совершен последний клик (значение обновляется после события Click, но до события CellClick).

```xml
<Object Name="DatabaseTableName">
  <Property Name="LastCellClickedRowIndex" />
</Object>
```

### LastCellClickedColumnName <a href="#get_last_cell_clicked_column_name" id="get_last_cell_clicked_column_name"></a>

Возвращает название столбца, по ячейке которого был совершен последний клик (значение обновляется после события Click, но до события CellClick).

```xml
<Object Name="DatabaseTableName">
  <Property Name="LastCellClickedColumnName" />
</Object>
```

### LastCellDoubleClickedRowIndex <a href="#get_last_cell_double_clicked_row_index" id="get_last_cell_double_clicked_row_index"></a>

Возвращает индекс строки, по ячейке которой был совершен последний двойной клик (значение обновляется после события [DoubleClick](../../conditions/event_condition/double_click_condition.md), но до события [CellDoubleClick](../../conditions/event_condition/cell_double_click_condition.md)).

```xml
<Object Name="DatabaseTableName">
  <Property Name="LastCellDoubleClickedRowIndex" />
</Object>
```

### LastCellDoubleClickedColumnName <a href="#get_last_cell_double_clicked_column_name" id="get_last_cell_double_clicked_column_name"></a>

Возвращает название столбца, по ячейке которого был совершен последний двойной клик (значение обновляется после события [DoubleClick](../../conditions/event_condition/double_click_condition.md), но до события [CellDoubleClick](../../conditions/event_condition/cell_double_click_condition.md)).

```xml
<Object Name="DatabaseTableName">
  <Property Name="LastCellDoubleClickedColumnName" />
</Object>
```

### LastCellValueChangedRowIndex <a href="#get_last_cell_value_changed_row_index" id="get_last_cell_value_changed_row_index"></a>

Возвращает индекс строки, ячейка которой была изменена последней (значение обновляется до события CellValueChanged).

```xml
<Object Name="DatabaseTableName">
  <Property Name="LastCellValueChangedRowIndex" />
</Object>
```

### LastCellValueChangedColumnName <a href="#get_last_cell_value_changed_column_name" id="get_last_cell_value_changed_column_name"></a>

Возвращает название столбца, ячейка которого была изменена последней (значение обновляется до события CellValueChanged).

```xml
<Object Name="DatabaseTableName">
  <Property Name="LastCellValueChangedColumnName" />
</Object>
```

### CellValue <a href="#get_cell_value" id="get_cell_value"></a>

Возвращает значение ячейки по индексу строки RowIndex и названию столбца ColumnName.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="CellValue">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным RowIndex: ожидается целое неотрицательное значение-->
      <Parameter Name="RowIndex">0</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
    </Parameters>
  </Property>
</Object>
```

### ColumnMinimumWidth <a href="#get_column_minimum_width" id="get_column_minimum_width"></a>

Возвращает минимальную ширину определенного столбца таблицы.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ColumnMinimumWidth">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
    </Parameters>
  </Property>
</Object>
```

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

### RowHeight <a href="#set_row_height" id="set_row_height"></a>

Задает высоту строк с данными в таблице.

Ожидается целочисленное значение.

```xml
<Object Name="DatabaseTableName">
  <Property Name="RowHeight">20</Property>
</Object>
```

### ColumnHeadersHeight <a href="#set_column_headers_height" id="set_column_headers_height"></a>

Задает высоту "шапки" таблицы.

Ожидается целочисленное значение.

```xml
<Object Name="DatabaseTableName">
  <Property Name="ColumnHeadersHeight">20</Property>
</Object>
```

### ColumnHeadersVisible <a href="#set_column_headers_visible" id="set_column_headers_visible"></a>

Задает признак, определяющий, показывать или нет "шапку" таблицы.

Ожидается логическое значение.

```xml
<Object Name="DatabaseTableName">
  <Property Name="ColumnHeadersVisible">True</Property>
</Object>
```

### RowHeadersWidth <a href="#set_row_headers_width" id="set_row_headers_width"></a>

Задает ширину "нулевого" столбца таблицы.

Ожидается целочисленное значение.

```xml
<Object Name="DatabaseTableName">
  <Property Name="RowHeadersWidth">200</Property>
</Object>
```

### RowHeadersVisible <a href="#set_row_headers_visible" id="set_row_headers_visible"></a>

Задает признак, определяющий, показывать или нет "нулевой" столбец таблицы.

Ожидается логическое значение.

```xml
<Object Name="DatabaseTableName">
  <Property Name="RowHeadersVisible">False</Property>
</Object>
```

### BackgroundColor <a href="#set_background_color" id="set_background_color"></a>

Задает имя цвета фона таблицы.

Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

```xml
<Object Name="DatabaseTableName">
  <Property Name="BackgroundColor">BackgroundColor</Property>
</Object>
```

### BorderStyle <a href="#set_border_style" id="set_border_style"></a>

Задает название типа границ таблицы.

Ожидается название одного из типов границ таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="BorderStyle">Fixed3D</Property>
</Object>
```

### CellBorderStyle <a href="#set_cell_border_style" id="set_cell_border_style"></a>

Задает название стиля границ ячеек в таблице.

Ожидается название одного из стилей границ ячеек в таблице.

```xml
<Object Name="DatabaseTableName">
  <Property Name="CellBorderStyle">SingleHorizontal</Property>
</Object>
```

### HideSelection <a href="#set_hide_selection" id="set_hide_selection"></a>

Задает признак видимости выделения в таблице.

Ожидается логическое значение.

```xml
<Object Name="DatabaseTableName">
  <Property Name="HideSelection">False</Property>
</Object>
```

### AllowInsert <a href="#set_allow_insert" id="set_allow_insert"></a>

Задает признак, определяющий, может ли пользователь добавлять строки в таблицу посредством графического интерфейса таблицы.

Ожидается логическое значение.

```xml
<Object Name="DatabaseTableName">
  <Property Name="AllowInsert">False</Property>
</Object>
```

### AllowUpdate <a href="#set_allow_update" id="set_allow_update"></a>

Задает признак, определяющий, может ли пользователь изменять значения в строках таблицы посредством графического интерфейса таблицы.

Ожидается логическое значение.

```xml
<Object Name="DatabaseTableName">
  <Property Name="AllowUpdate">False</Property>
</Object>
```

### AllowDelete <a href="#set_allow_delete" id="set_allow_delete"></a>

Задает признак, определяющий, может ли пользователь удалять строки из таблицы посредством графического интерфейса таблицы.

Ожидается логическое значение.

```xml
<Object Name="DatabaseTableName">
  <Property Name="AllowDelete">False</Property>
</Object>
```

### MultiSelect <a href="#set_multi_select" id="set_multi_select"></a>

Задает признак, определяющий, можно ли выделить в таблице более одной строки одновременно.

Ожидается логическое значение.

```xml
<Object Name="DatabaseTableName">
  <Property Name="MultiSelect">True</Property>
</Object>
```

### SelectionMode <a href="#set_selection_mode" id="set_selection_mode"></a>

Задает название типа выделения таблицы.

Ожидается название одного из типов выделения таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="SelectionMode">CellSelect</Property>
</Object>
```

### EditMode <a href="#set_edit_mode" id="set_edit_mode"></a>

Задает название типа редактирования ячеек таблицы.

Ожидается название одного из типов редактирования ячеек таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="EditMode">EditOnEnter</Property>
</Object>
```

### AllowResizeColumns <a href="#set_allow_resize_columns" id="set_allow_resize_columns"></a>

Задает признак, определяющий, может ли пользователь изменять ширину столбцов посредством графического интерфейса таблицы.

Ожидается логическое значение.

```xml
<Object Name="DatabaseTableName">
  <Property Name="AllowResizeColumns">False</Property>
</Object>
```

### AllowOrderColumns <a href="#set_allow_order_columns" id="set_allow_order_columns"></a>

Задает признак, определяющий, может ли пользователь изменять порядок столбцов посредством графического интерфейса таблицы.

Ожидается логическое значение.

```xml
<Object Name="DatabaseTableName">
  <Property Name="AllowOrderColumns">True</Property>
</Object>
```

### AllowResizeRows <a href="#set_allow_resize_rows" id="set_allow_resize_rows"></a>

Задает признак, определяющий, может ли пользователь изменять высоту строк посредством графического интерфейса таблицы.

Ожидается логическое значение.

```xml
<Object Name="DatabaseTableName">
  <Property Name="AllowResizeRows">True</Property>
</Object>
```

### AutoSizeRowsMode <a href="#set_auto_size_rows_mode" id="set_auto_size_rows_mode"></a>

Задает название типа автоматического изменения высот строк таблицы.

Ожидается название одного из типов автоматического изменения высот строк таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="AutoSizeRowsMode">AllCells</Property>
</Object>
```

### ColumnTitle <a href="#set_column_title" id="set_column_title"></a>

Задает название [`<Title>`](./#column_title) для столбца ColumnName таблицы.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ColumnTitle">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным Title: ожидается скалярное значение-->
      <Parameter Name="Title">Наименование</Parameter>
    </Parameters>
  </Property>
</Object>
```

### ColumnHint <a href="#set_column_hint" id="set_column_hint"></a>

Задает текст подсказки [`<Hint>`](./#column_hint), всплывающей на заголовке столбца таблицы, для столбца ColumnName таблицы.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ColumnHint">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным Hint: ожидается скалярное значение-->
      <Parameter Name="Hint">Текст подсказки</Parameter>
    </Parameters>
  </Property>
</Object>
```

### ColumnDisplayIndex <a href="#set_column_display_index" id="set_column_display_index"></a>

Задает порядок отображения [`<DisplayIndex>`](./#column_display_index) для столбца ColumnName таблицы.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ColumnDisplayIndex">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным DisplayIndex: ожидается неотрицательное целочисленное значение-->
      <Parameter Name="DisplayIndex">3</Parameter>
    </Parameters>
  </Property>
</Object>
```

### ColumnWidth <a href="#set_column_width" id="set_column_width"></a>

Задает ширину [`<Width>`](./#column_width) для столбца ColumnName таблицы.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ColumnWidth">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным Width: ожидается положительное целочисленное значение-->
      <Parameter Name="Width">100</Parameter>
    </Parameters>
  </Property>
</Object>
```

### SelectedRowIndex <a href="#set_selected_row_index" id="set_selected_row_index"></a>

Задает выделенную строку таблицы по индексу, показывая выделенную строку первой.

Ожидается целочисленное значение.

```xml
<Object Name="DatabaseTableName">
  <Property Name="SelectedRowIndex">1</Property>
</Object>
```

### SelectedRowsIndices <a href="#set_selected_rows_indices" id="set_selected_rows_indices"></a>

Задает выделенные строки таблицы по индексам.

Ожидается линейный массив целочисленных значений.

```xml
<Object Name="DatabaseTableName">
  <Property Name="SelectedRowsIndices">
    <Structure Type="List">
      <Item>1</Item>
      <Item>2</Item>
    </Structure>
  </Property>
</Object>
```

### SelectedColumnName <a href="#set_selected_column_name" id="set_selected_column_name"></a>

Задает выделенный столбец таблицы по имени.

Ожидается название одного из столбцов таблицы.

```xml
<Object Name="DatabaseTableName">
  <Property Name="SelectedColumnName">ColumnName</Property>
</Object>
```

### SelectedCellValue <a href="#set_selected_cell_value" id="set_selected_cell_value"></a>

Задает значение выделенной ячейки таблицы.

Ожидается любое значение.

```xml
<Object Name="DatabaseTableName">
  <Property Name="SelectedCellValue">Value</Property>
</Object>
```

### SelectCell <a href="#set_select_cell" id="set_select_cell"></a>

Выделяет ячейку по индексу строки и имени столбца.

```xml
<Object Name="DatabaseTable">
  <Property Name="SelectCell">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным RowIndex: ожидается целочисленное значение-->
      <Parameter Name="RowIndex" />
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName" />
    </Parameters>
  </Property>
</Object>
```

### SelectRowByFieldValue <a href="#set_select_row_by_field_value" id="set_select_row_by_field_value"></a>

Выделяет первую строку таблицы, для которой значение, указанное в столбце ColumnName, совпадает с одним из значений, указанных в параметре Value.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="SelectRowByFieldValue">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным Value: ожидается скалярное значение или линейных массив значений-->
      <Parameter Name="Value">Value</Parameter>
    </Parameters>
  </Property>
</Object>
```

### SelectRowsByFieldValue <a href="#set_select_rows_by_field_value" id="set_select_rows_by_field_value"></a>

Выделяет строки таблицы, для которых значений, указанные в столбце ColumnName, совпадают с одним из значений, указанных в параметре Value.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="SelectRowsByFieldValue">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным Value: ожидается скалярное значение или линейных массив значений-->
      <Parameter Name="Value">Value</Parameter>
    </Parameters>
  </Property>
</Object>
```

### AutoSize <a href="#set_auto_size" id="set_auto_size"></a>

Единоразово устанавливает ширину и высоту таблицы, сворачивая или разворачивая её таким образом, чтобы в зоне видимости оказались все её строки и столбцы без полос прокрутки.

Значение не ожидается.

```xml
<Object Name="DatabaseTableName">
  <Property Name="AutoSize" />
</Object>
```

### AddRow <a href="#set_add_row" id="set_add_row"></a>

Добавляет новую строку в таблицу со значениями Values, соответствующим столбцам ColumnNames, на место с индексом Index и выделяет ее в соответствии с признаком SelectAfterAdd, при этом снимая выделение с остальных строк в соответствии с признаком ClearOtherSelection.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="AddRow">
    <Parameters>
      <!--Необязательный параметр. При отсутствии используется пустой массив-->
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnNames: ожидается линейный массив названий столбцов таблицы-->
      <Parameter Name="ColumnNames">
        <Structure Type="List">
          <Item>ColumnName1</Item>
          <Item>ColumnName2</Item>
        </Structure>
      </Parameter>
      <!--Необязательный параметр. При отсутствии используется пустой массив-->
      <!--Значение тэга Parameter с атрибутом Name, равным Values: ожидается линейный массив любых значений-->
      <Parameter Name="Values">
        <Structure Type="List">
          <Item>Value1</Item>
          <Item>Value2</Item>
        </Structure>
      </Parameter>
      <!--Необязательный параметр. При отсутствии строка будет добавлена в конец таблицы-->
      <!--Значение тэга Parameter с атрибутом Name, равным Index: ожидается целое неотрицательное значение-->
      <Parameter Name="Index">0</Parameter>
      <!--Необязательный параметр. При отсутствии используется значение False-->
      <!--Значение тэга Parameter с атрибутом Name, равным SelectAfterAdd: ожидается логическое значение-->
      <Parameter Name="SelectAfterAdd">False</Parameter>
      <!--Необязательный параметр. При отсутствии используется значение True-->
      <!--Значение тэга Parameter с атрибутом Name, равным ClearOtherSelection: ожидается логическое значение-->
      <Parameter Name="ClearOtherSelection">True</Parameter>
    </Parameters>
  </Property>
</Object>
```

### AddRows <a href="#set_add_rows" id="set_add_rows"></a>

Добавляет новые строки в таблицу со значениями из таблицы Values, столбцы которой соответствуют столбцам ColumnNames, на места начиная с индекса Index и выделяя их (или первую из них - при значении тэга[`<MultiSelect>`](./#multi_select) равного False) в соответствии с признаком SelectAfterAdd, при этом выделение остальных строк снимается в соответствии с признаком ClearOtherSelection.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="AddRows">
    <Parameters>
      <!--Необязательный параметр. При отсутствии используется пустой массив-->
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnNames: ожидается линейный массив названий столбцов таблицы-->
      <Parameter Name="ColumnNames">
        <Structure Type="List">
          <Item>ColumnName1</Item>
          <Item>ColumnName2</Item>
        </Structure>
      </Parameter>
      <!--Необязательный параметр. При отсутствии используется пустая таблица-->
      <!--Значение тэга Parameter с атрибутом Name, равным Values: ожидается таблица (например, ссылка на GetDataConnection) с числом столбцов равным аналогичному числу из параметра ColumnNames-->
      <Parameter Name="Values">
        <DataConnection SourceDataConnection="SourceDataConnectionName">
          <Fields>
            <Field Name="ColumnName1" />
            <Field Name="ColumnName2" />
          </Fields>
        </DataConnection>
      </Parameter>
      <!--Необязательный параметр. При отсутствии строки будут добавлены в конец таблицы-->
      <!--Значение тэга Parameter с атрибутом Name, равным Index: ожидается целое неотрицательное значение-->
      <Parameter Name="Index">0</Parameter>
      <!--Необязательный параметр. При отсутствии используется значение False-->
      <!--Значение тэга Parameter с атрибутом Name, равным SelectAfterAdd: ожидается логическое значение-->
      <Parameter Name="SelectAfterAdd">False</Parameter>
      <!--Необязательный параметр. При отсутствии используется значение True-->
      <!--Значение тэга Parameter с атрибутом Name, равным ClearOtherSelection: ожидается логическое значение-->
      <Parameter Name="ClearOtherSelection">True</Parameter>
    </Parameters>
  </Property>
</Object>
```

### UpdateRow <a href="#set_update_row" id="set_update_row"></a>

Изменяет значения столбцов ColumnNames на значения Values, соответствующим столбцам ColumnNames, в строке с индексом RowIndex.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="UpdateRow">
    <Parameters>
      <!--Необязательный параметр. При отсутствии обновятся все строки-->
      <!--Значение тэга Parameter с атрибутом Name, равным RowIndex: ожидается целочисленное значение-->
      <Parameter Name="RowIndex">0</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnNames: ожидается линейный массив названий столбцов таблицы-->
      <Parameter Name="ColumnNames">
        <Structure Type="List">
          <Item>ColumnName1</Item>
          <Item>ColumnName2</Item>
        </Structure>
      </Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным Values: ожидается линейный массив любых значений-->
      <Parameter Name="Values">
        <Structure Type="List">
          <Item>Value1</Item>
          <Item>Value2</Item>
        </Structure>
      </Parameter>
    </Parameters>
  </Property>
</Object>
```

### UpdateRows <a href="#set_update_rows" id="set_update_rows"></a>

Изменяет значения столбцов ColumnNames на значения Values, соответствующим столбцам ColumnNames, в строках с индексами RowIndices.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="UpdateRows">
    <Parameters>
      <!--Необязательный параметр. При отсутствии обновятся все строки-->
      <!--Значение тэга Parameter с атрибутом Name, равным RowIndices: ожидается линейный массив целочисленных значений-->
      <Parameter Name="RowIndices">
        <Structure Type="List">
          <Item>1</Item>
          <Item>2</Item>
        </Structure>
      </Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnNames: ожидается линейный массив названий столбцов таблицы-->
      <Parameter Name="ColumnNames">
        <Structure Type="List">
          <Item>ColumnName1</Item>
          <Item>ColumnName2</Item>
        </Structure>
      </Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным Values: ожидается массив любых значений-->
      <Parameter Name="Values">
        <Structure Type="List">
          <Item>Value1</Item>
          <Item>Value2</Item>
        </Structure>
      </Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным ReplicateValues: ожидается логическое значение-->
      <!--Необязательный параметр. При отсутствии или значении True значение Values рассматривается как линейный массив значений, который изменяет строки с индексами RowIndices-->
      <!--Если параметр равен False, то значение Values рассматривается как матрица значений, которые будут записаны в строки с индексами RowIndices.-->
      <!--При этом:-->
      <!--   1. если количество элементов строки матрицы не совпадает с количеством столбцов ColumnNames, то значения недостающих ячеек изменяются на NULL;-->
      <!--   2. если количество строк матрицы не совпадает с количеством индексов RowIndices, то значения ячеек отсутствующих строк изменятся на NULL.-->
      <Parameter Name="ReplicateValues">False</Parameter>
    </Parameters>
  </Property>
</Object>
```

### UpdateColumn <a href="#set_update_column" id="set_update_column"></a>

Построчно изменяет значения ячеек в столбце ColumnName на соответствующие значения массива Values.

```xml
<!--Индекс обновляемой строки таблицы равен индексу ячейки массива, из которой новое значение будет взято-->
<!--Если длина массива меньше, чем количество строк в таблице, то оставшиеся без обновления строки будут заполнены пустыми значениями. Если длина массива больше, то оставшиеся значения будут проигнорированы-->
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="UpdateColumn">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным Values: ожидается линейный массив любых значений-->
      <Parameter Name="Values">
        <Structure Type="List">
          <Item>Value1</Item>
          <Item>Value2</Item>
        </Structure>
      </Parameter>
    </Parameters>
  </Property>
</Object>
```

### UpdateColumnCellsValues <a href="#set_update_column_cells_values" id="set_update_column_cells_values"></a>

Изменяет значения ячеек в строках с индексами RowsIndices в столбце ColumnName на значение Value.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="UpdateColumnCellsValues">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
      <!--Необязательный параметр. При отсутствии обновятся все строки-->
      <!--Значение тэга Parameter с атрибутом Name, равным RowsIndices: ожидается линейный массив любых значений-->
      <Parameter Name="RowsIndices">
        <Structure Type="List">
          <Item>Value1</Item>
          <Item>Value2</Item>
        </Structure>
      </Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным Value: ожидается любое значение-->
      <Parameter Name="Value">Value</Parameter>
    </Parameters>
  </Property>
</Object>
```

### DeleteRowsByIndices <a href="#set_delete_rows_by_indices" id="set_delete_rows_by_indices"></a>

Удаляет строки с индексами Value из таблицы.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="DeleteRowsByIndices">
    <Parameters>
      <!--Необязательный параметр. При отсутствии удалются все строки-->
      <!--Значение тэга Parameter с атрибутом Name, равным Value: ожидается линейный массив целочисленных значений-->
      <Parameter Name="Value">
        <Structure Type="List">
          <Item>1</Item>
          <Item>2</Item>
        </Structure>
      </Parameter>
    </Parameters>
  </Property>
</Object>
```

### ColumnMinimumWidth <a href="#set_column_minimum_width" id="set_column_minimum_width"></a>

Задает минимальную ширину [`<MinimumWidth>`](./#column_minium_width) для столбца ColumnName таблицы.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ColumnMinimumWidth">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ColumnName: ожидается название одного из столбцов таблицы-->
      <Parameter Name="ColumnName">ColumnName</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным Width: ожидается положительное целочисленное значение-->
      <Parameter Name="MinimumWidth">100</Parameter>
    </Parameters>
  </Property>
</Object>
```

### ClearSelection <a href="#set_clear_selection" id="set_clear_selection"></a>

Снимает выделение со всех строк таблицы.

Значение не ожидается.

```xml
<Object Name="DatabaseTableName">
   <Property Name="ClearSelection" />
</Object>
```

### ResetFilter

Принудительно сбрасывает все табличные фильтры, которые были заданы через контекстное меню таблицы.

Значение не ожидается.

```xml
<Object Name="DatabaseTableName">
   <Property Name="ResetFilter" />
</Object>
```
