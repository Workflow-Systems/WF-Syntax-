---
description: Графический объект; список файлов.
---

# FileListBox

## Шаблон FileListBox <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="" Type="FileListBox" Assembly="BaseControls" ChangeForm="">
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
  <!--Тэги, специфичные для FileListBox-->
  <View></View>
  <Sorting></Sorting>
  <MultiSelect></MultiSelect>
  <ShowTitle></ShowTitle>
  <AutoDownload></AutoDownload>
  <ShowThumbnails></ShowThumbnails>
  <ThumbnailWidth></ThumbnailWidth>
  <ThumbnailHeight></ThumbnailHeight>
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

## Описание FileListBox <a href="#description" id="description"></a>

```xml
<MyObject Name="FileListBoxName" Type="FileListBox" Assembly="BaseControls">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для FileListBox-->
</MyObject>
```

### Получение значения <a href="#get-value" id="get-value"></a>

Значением FileListBox считается реальное (не отображаемое, а именно реальное) значение выбранного элемента из списка.

```xml
<Object Name="FileListBoxName" />
```

### Задание значения <a href="#set-value" id="set-value"></a>

Значение объекта: любое значение.

```xml
<Object Name="FileListBoxName"></Object>
```

## Тэги, специфичные для FileListBox <a href="#specific-tags" id="specific-tags"></a>

### View <a href="#view" id="view"></a>

Название типа стиля отображения элементов в списке в списке.

Необязательный тэг. Ожидается название одного из типов стиля отображения элементов в списке:

<table data-header-hidden><thead><tr><th width="185" align="center"></th><th width="480.3333333333333"></th></tr></thead><tbody><tr><td align="center">LargeIcon</td><td>Каждый элемент отображается в виде полноразмерного значка с меткой под ним.</td></tr><tr><td align="center">SmallIcon</td><td>Каждый элемент отображается в виде небольшого значка с меткой справа.</td></tr><tr><td align="center">List</td><td>Каждый элемент отображается в виде небольшого значка с меткой справа. Элементы располагаются в столбцах без заголовков столбцов.</td></tr></tbody></table>

По умолчанию используется значение LargeIcon.

```xml
<View>LargeIcon</View>
```

### Sorting <a href="#sorting" id="sorting"></a>

Название типа сортировки элементов в списке.

Необязательный тэг. Ожидается название одного из типов сортировки элементов в списке:

<table data-header-hidden><thead><tr><th align="center"></th><th width="476.3333333333333"></th></tr></thead><tbody><tr><td align="center">None</td><td>Без сортировки</td></tr><tr><td align="center">Ascending</td><td>Сортировка по возрастанию</td></tr><tr><td align="center">Descending</td><td>Сортировка по убыванию</td></tr></tbody></table>

По умолчанию используется значение None.

```xml
<Sorting>None</Sorting>
```

### MultiSelect <a href="#multi_select" id="multi_select"></a>

Признак возможности выделения нескольких элементов списка.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<MultiSelect>False</MultiSelect>
```

### ShowTitle <a href="#show_title" id="show_title"></a>

Признак, определяющий, показывать ли названия файлов.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение True.

```xml
<ShowTitle>False</ShowTitle>
```

### AutoDownload <a href="#auto_download" id="auto_download"></a>

Признак, определяющий, скачивать ли удалённые файлы с сервера на локальный компьютер.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<AutoDownload>False</AutoDownload>
```

### ShowThumbnails <a href="#show_thumbnails" id="show_thumbnails"></a>

Признак, определяющий, показывать ли вместо иконки файла миниатюру с содержимом изображения.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<ShowThumbnails>False</ShowThumbnails>
```

### ThumbnailWidth <a href="#thumbnail_width" id="thumbnail_width"></a>

Ширина миниатюры.

Необязательный тэг. Ожидается целочисленное значение.

Если тэг `<ThumbnailWidth>` отсутствует, то используется значение 32.

```xml
<ThumbnailWidth>32</ThumbnailWidth>
```

### ThumbnailHeight <a href="#thumbnail_height" id="thumbnail_height"></a>

Высота миниатюры.

Необязательный тэг. Ожидается целочисленное значение.

Если тэг `<ThumbnailHeight>` отсутствует, то используется значение 32.

```xml
<ThumbnailHeight>32</ThumbnailHeight>
```

### ValueList <a href="#value_list" id="value_list"></a>

Элементы списка.

Необязательный тэг. Ожидается таблица с одним, двумя или более столбцами (например, ссылка на [GetDataConnection](../dataconnections/)).

Первое поле будет соответствовать реальному значению элемента, второе – его отображаемому значению (если второго поля нет, то отображаемое значение равно реальному). Все остальные поля игнорируются.

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

### View <a href="#get_view" id="get_view"></a>

Возвращает название типа стиля отображения элементов в списке.

```xml
<Object Name="FileListBoxName">
  <Property Name="View" />
</Object>
```

### Sorting <a href="#get_sorting" id="get_sorting"></a>

Возвращает название типа сортировки элементов в списке.

```xml
<Object Name="FileListBoxName">
  <Property Name="Sorting" />
</Object>
```

### MultiSelect <a href="#get_multi_select" id="get_multi_select"></a>

Возвращает признак возможности выделения нескольких элементов списка.

```xml
<Object Name="FileListBoxName">
  <Property Name="MultiSelect" />
</Object>
```

### ShowTitle <a href="#get_show_title" id="get_show_title"></a>

Возвращает признак, определяющий, показывать ли названия файлов.

```xml
<Object Name="FileListBoxName">
  <Property Name="ShowTitle" />
</Object>
```

### AutoDownload <a href="#get_auto_download" id="get_auto_download"></a>

Возвращает признак, определяющий, скачивать ли удалённые файлы с сервера на локальный компьютер.

```xml
<Object Name="FileListBoxName">
  <Property Name="AutoDownload" />
</Object>
```

### ShowThumbnails <a href="#get_show_thumbnails" id="get_show_thumbnails"></a>

Возвращает признак, определяющий, показывать ли вместо иконки файла миниатюру с содержимом изображения.

```xml
<Object Name="FileListBoxName">
  <Property Name="ShowThumbnails" />
</Object>
```

### ThumbnailWidth <a href="#get_thumbnail_width" id="get_thumbnail_width"></a>

Возвращает ширину миниатюры.

```xml
<Object Name="FileListBoxName">
  <Property Name="ThumbnailWidth" />
</Object>
```

### ThumbnailHeight <a href="#get_thumbnail_height" id="get_thumbnail_height"></a>

Возвращает высоту миниатюры.

```xml
<Object Name="FileListBoxName">
  <Property Name="ThumbnailHeight" />
</Object>
```

### ValueList <a href="#get_value_list" id="get_value_list"></a>

Возвращает элементы списка (таблица с двумя столбцами).

```xml
<Object Name="FileListBoxName">
  <Property Name="ValueList">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным Remote: любое значение будет переведено в логическое-->
      <!--Необязательный параметр. При отсутствии используется пустое значение -->
      <Parameter Name="Remote"></Parameter>
    </Parameters>
  </Property>
</Object>
```

### LocalValueList <a href="#get_local_value_list" id="get_local_value_list"></a>

Возвращает элементы списка с путями на локальные файлы (таблица с двумя столбцами).

```xml
<Object Name="FileListBoxName">
  <Property Name="LocalValueList">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным Remote: любое значение будет переведено в логическое-->
      <!--Необязательный параметр. При отсутствии используется пустое значение -->
      <Parameter Name="Remote"></Parameter>
    </Parameters>
  </Property>
</Object>
```

### SelectedCount <a href="#get_selected_count" id="get_selected_count"></a>

Возвращает количество выбранных элементов в списке.

```xml
<Object Name="FileListBoxName">
  <Property Name="SelectedCount" />
</Object>
```

### SelectedIndex <a href="#get_selected_index" id="get_selected_index"></a>

Возвращает индекс выбранного элемента.

```xml
<Object Name="FileListBoxName">
  <Property Name="SelectedIndex" />
</Object>
```

### SelectedIndices <a href="#get_selected_indices" id="get_selected_indices"></a>

Возвращает массив индексов выбранных элементов.

```xml
<Object Name="FileListBoxName">
  <Property Name="SelectedIndices" />
</Object>
```

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

### View <a href="#set_view" id="set_view"></a>

Задает название типа стиля отображения элементов в списке.

Ожидается название одного из типов стиля отображения элементов в списке.

```xml
<Object Name="FileListBoxName">
  <Property Name="View">List</Property>
</Object>
```

### Sorting <a href="#set_sorting" id="set_sorting"></a>

Задает название типа сортировки элементов в списке.

Ожидается название одного из типов сортировки элементов в списке.

```xml
<Object Name="FileListBoxName">
  <Property Name="Sorting">Ascending</Property>
</Object>
```

### MultiSelect <a href="#set_multi_select" id="set_multi_select"></a>

Задает признак возможности выделения нескольких элементов списка.

Ожидается логическое значение.

```xml
<Object Name="FileListBoxName">
  <Property Name="MultiSelect">True</Property>
</Object>
```

### ShowTitle <a href="#set_show_title" id="set_show_title"></a>

Задает признак, определяющий, показывать ли названия файлов.

Ожидается логическое значение.

```xml
<Object Name="FileListBoxName">
  <Property Name="ShowTitle">True</Property>
</Object>
```

### AutoDownload <a href="#set_auto_download" id="set_auto_download"></a>

Задаёт признак, определяющий, скачивать ли удалённые файлы с сервера на локальный компьютер.

Ожидается логическое значение.

```xml
<Object Name="FileListBoxName">
  <Property Name="AutoDownload">True</Property>
</Object>
```

### ShowThumbnails <a href="#set_show_thumbnails" id="set_show_thumbnails"></a>

Задаёт признак, определяющий, показывать ли вместо иконки файла миниатюру с содержимом изображения.

Ожидается логическое значение.

```xml
<Object Name="FileListBoxName">
  <Property Name="ShowThumbnails">True</Property>
</Object>
```

### ThumbnailWidth <a href="#set_thumbnail_width" id="set_thumbnail_width"></a>

Задаёт ширину миниатюры.

Ожидается числовое значение.

```xml
<Object Name="FileListBoxName">
  <Property Name="ThumbnailWidth">128</Property>
</Object>
```

### ThumbnailHeight <a href="#set_thumbnail_height" id="set_thumbnail_height"></a>

Задаёт высоту миниатюры.

Ожидается числовое значение.

```xml
<Object Name="FileListBoxName">
  <Property Name="ThumbnailHeight">128</Property>
</Object>
```

### AddFile <a href="#set_add_file" id="set_add_file"></a>

Добавляет файл в список.

```xml
<Object Name="FileListBoxName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="AddFile">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным Value: ожидается путь до файла, который будет добавлен в список-->
      <Parameter Name="Value">filename.ext</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным Title: любое значение будет переведено в текстовое-->
      <!--Необязательный параметр. При отсутствии используется пустая строка-->
      <Parameter Name="Title">filename.ext</Parameter>
    </Parameters>
  </Property>
</Object>
```

Возможен сокращенный вариант записи:

```xml
<Object Name="FileListBoxName">
  <!--Значение тэга Property: ожидается путь до файла, который будет добавлен в список-->
  <Property Name="AddFile">filename.ext</Property>
</Object>
```

### AddFiles <a href="#set_add_files" id="set_add_files"></a>

Добавляет несколько файлов в список.

```xml
<Object Name="FileListBoxName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="AddFiles">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным Value: ожидается матрица с двумя столбцами-->
      <Parameter Name="Value"></Parameter>
    </Parameters>
  </Property>
</Object>
```

### RemoveFileByIndex <a href="#set_remove_file_by_index" id="set_remove_file_by_index"></a>

Удаляет файл из списка.

Ожидается индекс элемента, который будет удалён.

```xml
<Object Name="FileListBoxName">
  <Property Name="RemoveFileByIndex">0</Property>
</Object>
```

### RemoveFilesByIndices <a href="#set_remove_files_by_indices" id="set_remove_files_by_indices"></a>

Удаляет файлы из списка.

Ожидается массив индексов элементов, которые будут удалены.

```xml
<Object Name="FileListBoxName">
  <Property Name="RemoveFilesByIndices">0</Property>
</Object>
```

### ValueList <a href="#set_value_list" id="set_value_list"></a>

Задает элементы списка.

Ожидается таблица с двумя столбцами (например, ссылка на [GetDataConnection](../dataconnections/) с указанием двух его полей).

```xml
<Object Name="FileListBoxName">
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
