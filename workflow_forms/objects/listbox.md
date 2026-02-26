---
description: Графический объект; список.
---

# ListBox

## Шаблон ListBox <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="" Type="ListBox" Assembly="BaseControls" ChangeForm="">
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
  <!--Тэги, специфичные для ListBox-->
  <Sorted></Sorted>
  <SelectionMode></SelectionMode>
  <NullValue Show="" Title="" />
  <Formatting>
    <BackColor Name="">
      <Expression></Expression>
      <Items>
        <Item></Item>
        <Item></Item>
      </Items>
    </BackColor>
    <ForeColor Name="">
      <Expression></Expression>
      <Items>
        <Item></Item>
        <Item></Item>
      </Items>
    </ForeColor>
  </Formatting>
  <ValueList>
    <DataConnection SourceDataConnection="">
      <Fields>
        <Field Name="" />
        <Field Name="" />
      </Fields>
    </DataConnection>
  </ValueList>
  <Value></Value>
</MyObject>
```

## Описание ListBox <a href="#description" id="description"></a>

```xml
<MyObject Name="ListBoxName" Type="ListBox" Assembly="BaseControls">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для ListBox-->
</MyObject>
```

### Получение значения <a href="#get-value" id="get-value"></a>

Значением ListBox считается реальное (не отображаемое, а именно реальное) значение выбранного элемента из списка.

```xml
<Object Name="ListBoxName" />
```

### Задание значения <a href="#set-value" id="set-value"></a>

Значение объекта: любое значение.

```xml
<Object Name="ListBoxName"></Object>
```

## Тэги, специфичные для ListBox <a href="#specific-tags" id="specific-tags"></a>

### Sorted <a href="#sorted" id="sorted"></a>

Признак сортировки элементов списка по отображаемым значениям.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<Sorted>False</Sorted>
```

### SelectionMode <a href="#selection_mode" id="selection_mode"></a>

Название типа выбора элементов в списке.

Необязательный тэг. Ожидается название одного из типов выбора элементов в списке:

<table data-header-hidden><thead><tr><th align="center"></th><th width="443"></th></tr></thead><tbody><tr><td align="center">None</td><td>Выделение элементов запрещено</td></tr><tr><td align="center">One</td><td>Разрешено выделение только одного элемента</td></tr><tr><td align="center">MultiSimple</td><td>Разрешено выделение нескольких элементов</td></tr><tr><td align="center">MultiExtended</td><td>Разрешено выделение нескольких элементов, и пользователь может производить выделение с помощью клавиши SHIFT, клавиши CTRL и клавиш со стрелками</td></tr></tbody></table>

По умолчанию используется значение One.

```xml
<SelectionMode>One</SelectionMode>
```

### NullValue <a href="#null_value" id="null_value"></a>

Настройка отображения NULL-значения объекта.

Необязательный тэг. Значение тэга `<NullValue>`: не ожидается.

Если тэг `<NullValue>` отсутствует, то для атрибута `Show` используется значение False.

```xml
<NullValue Show="" Title="" />
```

#### Атрибуты тэга `<NullValue>` <a href="#attributes_tag_null_value" id="attributes_tag_null_value"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="426"></th></tr></thead><tbody><tr><td align="center">Show</td><td><p>Признак, определяющий, будет ли в списке элемент, имеющий реальное значение NULL.</p><p></p><p>Необязательный атрибут. Ожидается логическое значение.</p><p></p><p>По умолчанию используется значение False.</p></td></tr><tr><td align="center">Title</td><td><p>Отображаемое значение элемента, имеющего реальное значение NULL.</p><p></p><p>Необязательный атрибут. Любое значение будет переведено в текстовое.</p><p></p><p>По умолчанию используется пустое значение.</p></td></tr></tbody></table>

### Formatting <a href="#formatting" id="formatting"></a>

Условное форматирование элементов выпадающего списка на основе значений хранящихся в них данных.

Необязательный тэг. Значение тэга `<Formatting>`: список тэгов [`<BackColor>`](listbox.md#formatting_back_color) и [`<ForeColor>`](listbox.md#formatting_fore_color).

```xml
<Formatting>
  <BackColor Name="BackColor">
    <Expression>[0] > {0} * {1}</Expression>
    <Items>
      <Item>10</Item>
      <Item>20</Item>
    </Items>
  </BackColor>
  <ForeColor Name="ForeColor">
    <Expression>[0] > {0} * {1}</Expression>
    <Items>
      <Item>10</Item>
      <Item>20</Item>
    </Items>
  </ForeColor>
</Formatting>
```

#### Тэг `<BackColor>` <a href="#formatting_back_color" id="formatting_back_color"></a>

Используется в тэге [`<Formatting>`](listbox.md#formatting).

Условный цвет фона элемента списка.&#x20;

Необязательный тэг. Значение тэга `<BackColor>`: не ожидается.

#### Атрибуты тэга `<BackColor>` <a href="#attributes_tag_back_color" id="attributes_tag_back_color"></a>

<table data-header-hidden><thead><tr><th width="150" align="center"></th><th width="434"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).</p></td></tr></tbody></table>

#### Тэг `<Expression>` <a href="#formatting_expression" id="formatting_expression"></a>

Выражение для вычисления, возвращающее логическое значение, на основе которого форматирование будет применено или нет.

Обязательный тэг. Значение тэга `<Expression>`: любое значение.

Выражение для вычисления поддерживает переменные вида "\[N]", где N – порядковый номер столбца в таблице элементов списка (0 – реальное значение, 1 – отображаемое, 2-... – все остальные).

Выражение для вычисления поддерживает переменные вида "{N}" для подстановки значений (N+1)-ого элемента, то есть {0}, {1} и т.д.

Все поддерживаемые в выражении для вычисления конструкции смотрите по ссылке [https://ncalc.codeplex.com/wikipage?title=functions](https://ncalc.codeplex.com/wikipage?title=functions).

#### Тэг `<Items>` <a href="#formatting_back_color_items" id="formatting_back_color_items"></a>

Переменные для подстановки в выражение для вычисления.

Необязательный тэг. Значение тэга `<Items>`: список тэгов [`<Item>`](listbox.md#formatting_back_color_items_item).

#### Тэг `<Item>` <a href="#formatting_back_color_items_item" id="formatting_back_color_items_item"></a>

Переменная для подстановки в выражение для вычисления.

Необязательный тэг. Значение тэга `<Item>`: любое значение.

#### Тэг `<ForeColor>` <a href="#formatting_fore_color" id="formatting_fore_color"></a>

Используется в тэге [`<Formatting>`](listbox.md#formatting).

Условный цвет шрифта элемента списка.

Необязательный тэг. Значение тэга `<ForeColor>`: не ожидается.

#### Атрибуты тэга `<ForeColor>` <a href="#attributes_tag_fore_color" id="attributes_tag_fore_color"></a>

<table data-header-hidden><thead><tr><th width="150" align="center"></th><th width="434"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).</p></td></tr></tbody></table>

#### Тэг `<Expression>` <a href="#formatting_fore_color_expression" id="formatting_fore_color_expression"></a>

Выражение для вычисления, возвращающее логическое значение, на основе которого форматирование будет применено или нет.

Обязательный тэг. Значение тэга `<Expression>`: любое значение.

Выражение для вычисления поддерживает переменные вида "\[N]", где N – порядковый номер столбца в таблице элементов списка (0 – реальное значение, 1 – отображаемое, 2-... – все остальные).

Выражение для вычисления поддерживает переменные вида "{N}" для подстановки значений (N+1)-ого элемента, то есть {0}, {1} и т.д.

Все поддерживаемые в выражении для вычисления конструкции смотрите по ссылке [https://ncalc.codeplex.com/wikipage?title=functions](https://ncalc.codeplex.com/wikipage?title=functions).

#### Тэг `<Items>` <a href="#formatting_fore_color_items" id="formatting_fore_color_items"></a>

Переменные для подстановки в выражение для вычисления.

Необязательный тэг. Значение тэга `<Items>`: список тэгов [`<Item>`](listbox.md#formatting_fore_color_items_item).

#### Тэг `<Item>` <a href="#formatting_fore_color_items_item" id="formatting_fore_color_items_item"></a>

Переменная для подстановки в выражение для вычисления.

Необязательный тэг. Значение тэга `<Item>`: любое значение.

### ValueList <a href="#value_list" id="value_list"></a>

Элементы списка.

Необязательный тэг. Ожидается таблица с одним, двумя или более столбцами (например, ссылка на [`GetDataConnection`](../dataconnections/)).

Первое поле будет соответствовать реальному значению элемента, второе – его отображаемому значению (если второго поля нет, то отображаемое значение равно реальному).

Все остальные поля могут быть опционально использованы в выражениях для условного форматирования элементов списка.

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

### Value <a href="#value" id="value"></a>

Значение, соответствующее реальному значению выделенного элемента.

Необязательный тэг. Значение тэга `<Value>`: любое значение.

```xml
<Value>Value</Value>
```

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### Sorted <a href="#get_sorted" id="get_sorted"></a>

Возвращает признак сортировки элементов списка по отображаемым значениям.

```xml
<Object Name="ListBoxName">
  <Property Name="Sorted" />
</Object>
```

### SelectionMode <a href="#get_selection_mode" id="get_selection_mode"></a>

Возвращает название типа выбора элементов в списке.

```xml
<Object Name="ListBoxName">
  <Property Name="SelectionMode" />
</Object>
```

### Text <a href="#get_text" id="get_text"></a>

Возвращает отображаемое значение выбранного элемента.

```xml
<Object Name="ListBoxName">
  <Property Name="Text" />
</Object>
```

### ValueList <a href="#get_value_list" id="get_value_list"></a>

Возвращает элементы списка (таблица с двумя столбцами).

```xml
<Object Name="ListBoxName">
  <Property Name="ValueList" />
</Object>
```

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

### Sorted <a href="#set_sorted" id="set_sorted"></a>

Задает признак сортировки элементов списка по отображаемым значениям.

Ожидается логическое значение.

```xml
<Object Name="ListBoxName">
  <Property Name="Sorted">True</Property>
</Object>
```

### SelectionMode <a href="#set_selection_mode" id="set_selection_mode"></a>

Задает название типа выбора элементов в списке.

Ожидается название одного из типов выбора элементов в списке.

```xml
<Object Name="ListBoxName">
  <Property Name="SelectionMode">MultiExtended</Property>
</Object>
```

### ValueList <a href="#set_value_list" id="set_value_list"></a>

Задает элементы списка.

Ожидается таблица с двумя столбцами (например, ссылка на [`GetDataConnection`](../dataconnections/) с указанием двух его полей).

```xml
<Object Name="ComboBoxName">
  <Property Name="ValueList">
    <DataConnection SourceDataConnection="SourceDataConnectionName">
      <Fields>
        <Field Name="Field1Name" />
        <Field Name="Field2Name" />
      </Fields>
    </DataConnection>
  </Property>
</Object>
```
