---
description: Графический объект; поле с выпадающим списком.
---

# ComboBox

## Шаблон ComboBox <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="" Type="ComboBox" Assembly="BaseControls" ChangeForm="">
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
  <!--Тэги, специфичные для ComboBox-->
  <EnterText></EnterText>
  <MaxLength></MaxLength>
  <AutoCompleteMode></AutoCompleteMode>
  <AutoCompleteSource></AutoCompleteSource>
  <Sorted></Sorted>
  <DropDownHeight></DropDownHeight>
  <DropDownWidth></DropDownWidth>
  <InputLanguage></InputLanguage>
  <InputCase></InputCase>
  <FlatStyle></FlatStyle>
  <NullValue Show="" Title="" />
  <NullValueTitle></NullValueTitle>
  <AllowOutOfList Value="" />
  <SelectFirstOnPressEnter></SelectFirstOnPressEnter>
  <Text></Text>
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

## Описание ComboBox <a href="#description" id="description"></a>

```xml
<MyObject Name="ComboBoxName" Type="ComboBox" Assembly="BaseControls">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для ComboBox-->
</MyObject>
```

### Получение значения <a href="#get-value" id="get-value"></a>

Значением ComboBox считается реальное значение выбранного элемента из списка.

```xml
<Object Name="ComboBoxName" />
```

### Задание значения <a href="#set-value" id="set-value"></a>

Значение объекта: любое значение.

```xml
<Object Name="ComboBoxName"></Object>
```

## Тэги, специфичные для ComboBox <a href="#specific-tags" id="specific-tags"></a>

### EnterText <a href="#enter_text" id="enter_text"></a>

Признак, определяющий, может ли пользователь вводить текст внутри поля.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<EnterText>False</EnterText>
```

### MaxLength <a href="#max_length" id="max_length"></a>

Задает максимальное число символов, которое разрешается вводить или вставлять в поле.

Необязательный тэг. Ожидается положительное целочисленное значение.

По умолчанию используется значение 0, показывающее, что ограничения нет.

```xml
<MaxLength>0</MaxLength>
```

### AutoCompleteMode <a href="#auto_complete_mode" id="auto_complete_mode"></a>

Название типа автоматического завершения ввода содержимого поля.

Необязательный тэг. Ожидается название одного из типов автоматического завершения ввода содержимого:

<table data-header-hidden><thead><tr><th align="center"></th><th width="499.3333333333333"></th></tr></thead><tbody><tr><td align="center">None</td><td>Нет автоматического завершения</td></tr><tr><td align="center">Suggest</td><td>При вводе появляется список значений, совпадающих по началу (без учета регистра) с текущим значением поля</td></tr><tr><td align="center">Append</td><td>При вводе в поле появляется подсвеченное окончание значения, соответствующее элементу выпадающего списка, совпадающим по началу с текущим значением поля</td></tr><tr><td align="center">SuggestAppend</td><td>Применение обеих настроек Suggest и Append</td></tr><tr><td align="center">SmartSuggest</td><td>При вводе появляется список значений, хотя бы частично совпадающих (без учета регистра) с текущим значением поля</td></tr></tbody></table>

По умолчанию используется значение None.

```xml
<AutoCompleteMode>None</AutoCompleteMode>
```

### AutoCompleteSource <a href="#auto_complete_source" id="auto_complete_source"></a>

Название типа источника данных для завершения ввода содержимого поля.

Необязательный тэг. Ожидается название одного из типов источников данных для завершения ввода содержимого:

<table data-header-hidden><thead><tr><th width="225.91801715919928" align="center"></th><th width="499.3333333333333"></th></tr></thead><tbody><tr><td align="center">FileSystem</td><td>Файловая система</td></tr><tr><td align="center">HistoryList</td><td>Список истории посещенных URL-адресов</td></tr><tr><td align="center">RecentlyUsedList</td><td>Список недавно посещенных URL-адресов</td></tr><tr><td align="center">AllUrl</td><td>Объединяет обе настройки HistoryList и RecentlyUsedList</td></tr><tr><td align="center">AllSystemSources</td><td>Объединяет обе настройки FileSystem и AllUrl</td></tr><tr><td align="center">FileSystemDirectories</td><td>Только папки файловой системы</td></tr><tr><td align="center">CustomSource</td><td>Указанный источник</td></tr><tr><td align="center">None</td><td>Нет источника. Если AutoCompleteMode не SmartSuggest, то автозаполнения не будет</td></tr><tr><td align="center">ListItems</td><td>Значения выпадающего списка</td></tr></tbody></table>

По умолчанию используется значение None.

```xml
<AutoCompleteSource>None</AutoCompleteSource>
```

### Sorted <a href="#sorted" id="sorted"></a>

Признак сортировки элементов выпадающего списка по отображаемым значениям.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<Sorted>False</Sorted>
```

### DropDownHeight <a href="#drop_down_height" id="drop_down_height"></a>

Высота выпадающего списка.

Необязательный тэг. Ожидается целочисленное значение.

По умолчанию используется стандартное значение .NET.

```xml
<DropDownHeight>100</DropDownHeight>
```

### DropDownWidth <a href="#drop_down_width" id="drop_down_width"></a>

Ширина выпадающего списка.

Необязательный тэг. Ожидается целочисленное значение.

По умолчанию используется значение ширины объекта.

```xml
<DropDownWidth>200</DropDownWidth>
```

### InputLanguage <a href="#input_language" id="input_language"></a>

Название языка для ограничения по вводимым символам.

Необязательный тэг. Ожидается название одного из языков:

<table data-header-hidden><thead><tr><th align="center"></th><th width="435.6666666666667"></th></tr></thead><tbody><tr><td align="center">Rus</td><td>Русский</td></tr><tr><td align="center">Eng</td><td>Английский</td></tr><tr><td align="center">None</td><td>Без ограничений по языку</td></tr></tbody></table>

По умолчанию используется значение None.

Если язык вводимого символа не совпадает с языком, указанном в данном тэге, то этот символ будет трансформирован в символ другого языка, расположенный на этой же клавише на клавиатуре.

```xml
<InputLanguage>None</InputLanguage>
```

### InputCase <a href="#input_case" id="input_case"></a>

Название типа регистра для ограничения по вводимым символам.

Необязательный тэг. Ожидается название одного из типов регистров:

<table data-header-hidden><thead><tr><th align="center"></th><th width="435.6666666666667"></th></tr></thead><tbody><tr><td align="center">Upper</td><td>Верхний регистр</td></tr><tr><td align="center">Lower</td><td>Нижний регистр</td></tr><tr><td align="center">None</td><td>Без ограничений по регистру</td></tr></tbody></table>

По умолчанию используется значение None.

Если регистр вводимого символа не совпадает с регистром, указанном в данном тэге, то этот символ будет трансформирован в указанный регистр.

```xml
<InputCase>None</InputCase>
```

### FlatStyle <a href="#flat_style" id="flat_style"></a>

Название типа границ поля.

Необязательный тэг. Ожидается название одного из стилей отображения поля:

<table data-header-hidden><thead><tr><th align="center"></th><th width="435.6666666666667"></th></tr></thead><tbody><tr><td align="center">Flat</td><td>Плоское</td></tr><tr><td align="center">Popup</td><td>Плоское, пока не наведена мышь</td></tr><tr><td align="center">Standard</td><td>Обычное</td></tr><tr><td align="center">System</td><td>Определяется операционной системой</td></tr></tbody></table>

По умолчанию используется значение Standard.

```xml
<FlatStyle>Standard</FlatStyle>
```

### Text

Текст поля (доступно в случае, если [`<EnterText>`](combobox.md#enter_text) имеет значение True).

Необязательный тэг. Любое значение будет переведено в текстовое.

Текстовое значение может быть присвоено, только если основное значение [`<Value>`](combobox.md#value) равно NULL.

```xml
<Text>Текст</Text>
```

### NullValue <a href="#null_value" id="null_value"></a>

Настройка отображения NULL-значения объекта.

Необязательный тэг. Значение тэга не ожидается.

Если тэг `<NullValue>` отсутствует, то для атрибута `Show` используется значение False.

```xml
<NullValue Show="False" Title="[не выбрано]" />
```

<table data-header-hidden><thead><tr><th width="150" align="center"></th><th width="435.6666666666667"></th></tr></thead><tbody><tr><td align="center">Show</td><td><p>Признак, определяющий, будет ли в выпадающем списке элемент, имеющий реальное значение NULL.</p><p></p><p>Необязательный атрибут. Ожидается логическое значение.</p><p></p><p>По умолчанию используется значение False.</p></td></tr><tr><td align="center">Title</td><td><p>Отображаемое значение элемента, имеющего реальное значение NULL.</p><p></p><p>Необязательный атрибут. Любое значение будет переведено в текстовое.</p><p></p><p>По умолчанию используется пустое значение.</p></td></tr></tbody></table>

### NullValueTitle <a href="#null_value_title" id="null_value_title"></a>

Отображаемое значение элемента, имеющего реальное значение NULL.

Необязательный тэг. Любое значение будет переведено в текстовое.

По умолчанию используется пустое значение.

Игнорируется при наличии атрибута `Title` в тэге [`<NullValue>`](combobox.md#null_value).

```xml
<NullValueTitle>[не выбрано]</NullValueTitle>
```

### AllowOutOfList <a href="#allow_out_of_list" id="allow_out_of_list"></a>

Признак, разрешающий полю принимать и хранить значение даже если это значение отсутствует в списке элементов поля.

Необязательный тэг. Значение тэга не ожидается.

Обязательный атрибут `Value` ожидает логическое значение.

По умолчанию для атрибута `Value` используется значение False.

```xml
<AllowOutOfList Value="False" />
```

### SelectFirstOnPressEnter <a href="#select_first_on_press_enter" id="select_first_on_press_enter"></a>

Признак, включающий механизм выбора первого значения при нажатии клавиши Enter, если в выпадающем списке не выбрано значение.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение True.

```xml
<SelectFirstOnPressEnter>False</SelectFirstOnPressEnter>
```

### Formatting <a href="#formatting" id="formatting"></a>

Условное форматирование элементов выпадающего списка на основе значений хранящихся в них данных.

Необязательный тэг. Значение тэга `<Formatting>`: список тэгов [`<BackColor>`](combobox.md#formatting_back_color) и [`<ForeColor>`](combobox.md#formatting_fore_color).

```xml
<Formatting>
  <BackColor Name="BackColorName">
    <Expression>[0] > {0} * {1}</Expression>
    <Items>
      <Item>10</Item>
      <Item>20</Item>
    </Items>
  </BackColor>
  <ForeColor Name="ForeColorName">
    <Expression>[0] > {0} * {1}</Expression>
    <Items>
      <Item>10</Item>
      <Item>20</Item>
    </Items>
  </ForeColor>
</Formatting>
```

#### Тэг \<BackColor> <a href="#formatting_back_color" id="formatting_back_color"></a>

Используется в тэге [`<Formatting>`](combobox.md#formatting).

Условный цвет фона элемента списка. Необязательный тэг.

Значение тэга `<BackColor>`: не ожидается.

#### Атрибуты тэга`<BackColor>` <a href="#attributes_tag_back_color" id="attributes_tag_back_color"></a>

<table data-header-hidden><thead><tr><th width="150" align="center"></th><th width="434"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).</p></td></tr></tbody></table>

#### Тэг `<Expression>` <a href="#formatting_back_color_expression" id="formatting_back_color_expression"></a>

Выражение для вычисления, возвращающее логическое значение, на основе которого форматирование будет применено или нет.

Обязательный тэг. Значение тэга `<Expression>`: любое значение.

Выражение для вычисления поддерживает переменные вида "\[N]", где N – порядковый номер столбца в таблице элементов списка (0 – реальное значение, 1 – отображаемое, 2-... – все остальные).

Выражение для вычисления поддерживает переменные вида "{N}" для подстановки значений (N+1)-ого элемента, то есть {0}, {1} и т.д.

Все поддерживаемые в выражении для вычисления конструкции смотрите по ссылке [https://ncalc.codeplex.com/wikipage?title=functions](https://ncalc.codeplex.com/wikipage?title=functions).

#### Тэг `<Items>` <a href="#formatting_back_color_items" id="formatting_back_color_items"></a>

Переменные для подстановки в выражение для вычисления.

Необязательный тэг. Значение тэга `<Items>`: список тэгов [`<Item>`](combobox.md#formatting_back_color_items_item).

#### Тэг `<Item>` <a href="#formatting_back_color_items_item" id="formatting_back_color_items_item"></a>

Переменная для подстановки в выражение для вычисления.

Необязательный тэг. Значение тэга `<Item>`: любое значение.

#### Тэг `<ForeColor>` <a href="#formatting_fore_color" id="formatting_fore_color"></a>

Используется в тэге [`<Formatting>`](combobox.md#formatting).

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

Необязательный тэг. Значение тэга `<Items>`: список тэгов [`<Item>`](combobox.md#formatting_fore_color_items_item).

#### Тэг `<Item>` <a href="#formatting_fore_color_items_item" id="formatting_fore_color_items_item"></a>

Переменная для подстановки в выражение для вычисления.

Необязательный тэг. Значение тэга `<Item>`: любое значение.

### ValueList <a href="#value_list" id="value_list"></a>

Элементы выпадающего списка.

Необязательный тэг. Ожидается таблица с одним, двумя или более столбцами (например, ссылка на [`GetDataConnection`](../dataconnections/)).

Первое поле будет соответствовать реальному значению элемента, второе – его отображаемому значению (если второго поля нет, то отображаемое значение равно реальному).

Все остальные поля могут быть опционально использованы в выражениях для условного форматирования элементов выпадающего списка.

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

Значение, соответствующее реальному значению выбранного элемента.

Необязательный тэг. Значение тэга `<Value>`: любое значение.

Если введенное в поле текстовое значение совпадает по отображаемому значению с одним из элементов выпадающего списка, то значение объекта равно реальному значению соответствующего элемента выпадающего списка, иначе - введенному в поле значению.

```xml
<Value>Value</Value>
```

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### EnterText <a href="#get_enter_text" id="get_enter_text"></a>

Возвращает признак, определяющий, может ли пользователь вводить текст внутри поля.

```xml
<Object Name="ComboBoxName">
  <Property Name="EnterText" />
</Object>
```

### MaxLength <a href="#get_max_length" id="get_max_length"></a>

Возвращает количество символов, которые пользователь может ввести внутри поля.

```xml
<Object Name="ComboBoxName">
  <Property Name="MaxLength" />
</Object>
```

### AutoCompleteMode <a href="#get_auto_complete_mode" id="get_auto_complete_mode"></a>

Возвращает название типа автоматического завершения ввода содержимого поля.

```xml
<Object Name="ComboBoxName">
  <Property Name="AutoCompleteMode" />
</Object>
```

### AutoCompleteSource <a href="#get_auto_complete_source" id="get_auto_complete_source"></a>

Возвращает название типа источника данных для завершения ввода содержимого поля.

```xml
<Object Name="ComboBoxName">
  <Property Name="AutoCompleteSource" />
</Object>
```

### Sorted <a href="#get_sorted" id="get_sorted"></a>

Возвращает признак сортировки элементов выпадающего списка по отображаемым значениям.

```xml
<Object Name="ComboBoxName">
  <Property Name="Sorted" />
</Object>
```

### DropDownHeight <a href="#get_drop_down_height" id="get_drop_down_height"></a>

Возвращает высоту выпадающего списка.

```xml
<Object Name="ComboBoxName">
  <Property Name="DropDownHeight" />
</Object>
```

### DropDownWidth <a href="#get_drop_down_width" id="get_drop_down_width"></a>

Возвращает ширину выпадающего списка.

```xml
<Object Name="ComboBoxName">
  <Property Name="DropDownWidth" />
</Object>
```

### InputLanguage <a href="#get_input_language" id="get_input_language"></a>

Возвращает название языка для ограничения по вводимым символам.

```xml
<Object Name="ComboBoxName">
  <Property Name="InputLanguage" />
</Object>
```

### InputCase <a href="#get_input_case" id="get_input_case"></a>

Возвращает название типа регистра для ограничения по вводимым символам.

```xml
<Object Name="ComboBoxName">
  <Property Name="InputCase" />
</Object>
```

### FlatStyle <a href="#get_flat_style" id="get_flat_style"></a>

Возвращает название типа границ поля.

```xml
<Object Name="ComboBoxName">
  <Property Name="FlatStyle" />
</Object>
```

### Text <a href="#get_text" id="get_text"></a>

Возвращает отображаемое значение поля только в том случае, если реальное значение [`<Value>`](combobox.md#value) возвращает NULL.

```xml
<Object Name="ComboBoxName">
  <Property Name="Text" />
</Object>
```

### VisibleText <a href="#get_visible_text" id="get_visible_text"></a>

Возвращает отображаемое значение поля.

```xml
<Object Name="ComboBoxName">
  <Property Name="VisibleText" />
</Object>
```

### Percentage <a href="#get_percentage" id="get_percentage"></a>

Возвращает значение в процентах от отображаемого значения поля (например, при отображаемом значении "0,95" проперти Percentage вернет 95).

```xml
<Object Name="ComboBoxName">
  <Property Name="Percentage" />
</Object>
```

### Length <a href="#get_length" id="get_length"></a>

Возвращает длину отображаемого текста поля.

```xml
<Object Name="ComboBoxName">
  <Property Name="Length" />
</Object>
```

### ValueList <a href="#get_value_list" id="get_value_list"></a>

Возвращает элементы выпадающего списка (таблица с двумя столбцами).

```xml
<Object Name="ComboBoxName">
  <Property Name="ValueList" />
</Object>
```

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

### EnterText <a href="#set_enter_text" id="set_enter_text"></a>

Задает признак, определяющий, может ли пользователь вводить текст внутри поля.

Ожидается логическое значение.

```xml
<Object Name="ComboBoxName">
  <Property Name="EnterText">True</Property>
</Object>
```

### MaxLength <a href="#set_max_length" id="set_max_length"></a>

Задает количество символов, которые пользователь может ввести внутри поля.

Ожидается целочисленное значение.

```xml
<Object Name="ComboBoxName">
  <Property Name="MaxLength">200</Property>
</Object>
```

### AutoCompleteMode <a href="#set_auto_complete_mode" id="set_auto_complete_mode"></a>

Задает название типа автоматического завершения ввода содержимого поля.

Ожидается название одного из типов автоматического завершения ввода содержимого.

```xml
<Object Name="ComboBoxName">
  <Property Name="AutoCompleteMode">Append</Property>
</Object>
```

### AutoCompleteSource <a href="#set_auto_complete_source" id="set_auto_complete_source"></a>

Задает название типа источника данных для завершения ввода содержимого поля.

Ожидается название одного из типов источников данных для завершения ввода содержимого.

```xml
<Object Name="ComboBoxName">
  <Property Name="AutoCompleteSource">ListItems</Property>
</Object>
```

### Sorted <a href="#set_sorted" id="set_sorted"></a>

Задает признак сортировки элементов выпадающего списка по отображаемым значениям.

Ожидается логическое значение.

```xml
<Object Name="ComboBoxName">
  <Property Name="Sorted">True</Property>
</Object>
```

### DropDownHeight <a href="#set_drop_down_height" id="set_drop_down_height"></a>

Задает высоту выпадающего списка.

Ожидается целочисленное значение.

```xml
<Object Name="ComboBoxName">
  <Property Name="DropDownHeight">400</Property>
</Object>
```

### DropDownWidth <a href="#set_drop_down_width" id="set_drop_down_width"></a>

Задает ширину выпадающего списка.

Ожидается целочисленное значение.

```xml
<Object Name="ComboBoxName">
  <Property Name="DropDownWidth">300</Property>
</Object>
```

### InputLanguage <a href="#set_input_language" id="set_input_language"></a>

Задает название языка для ограничения по вводимым символам.

Ожидается один из языков.

```xml
<Object Name="ComboBoxName">
  <Property Name="InputLanguage">Rus</Property>
</Object>
```

### InputCase <a href="#set_input_case" id="set_input_case"></a>

Задает название типа регистра для ограничения по вводимым символам.

Ожидается один из типов регистров.

```xml
<Object Name="ComboBoxName">
  <Property Name="InputCase">Lower</Property>
</Object>
```

### FlatStyle <a href="#set_flat_style" id="set_flat_style"></a>

Задает название типа границ поля.

Ожидается одно из названий типов границ поля.

```xml
<Object Name="ComboBoxName">
  <Property Name="FlatStyle">Popup</Property>
</Object>
```

### Text <a href="#set_text" id="set_text"></a>

Задает отображаемое значение поля.

Любое значение будет переведено в текстовое.

Текстовое значение может быть присвоено только если основное значение [`<Value>`](combobox.md#value) равно NULL.

```xml
<Object Name="ComboBoxName">
  <Property Name="Text">Текст</Property>
</Object>
```

### ValueList <a href="#set_value_list" id="set_value_list"></a>

Задает элементы выпадающего списка.

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
