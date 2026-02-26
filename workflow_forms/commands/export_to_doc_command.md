---
description: >-
  Команда; генерирует DOC-файл из шаблона, в котором вместо переменных
  подставляются определенные значения.
---

# ExportToDocCommand

## Поддерживаемые переменные <a href="#supported_variables" id="supported_variables"></a>

### <#variable#> <a href="#variable_scalar" id="variable_scalar"></a>

Служит для отображения скалярного значения.

### <%variable%> <a href="#variable_array" id="variable_array"></a>

Служит для отображения массива (для использования в таблице).

### <\~variable\~> <a href="#variable_document" id="variable_document"></a>

Служит для полного переноса содержимого другого документа (подшаблона) в шаблон.

В тексте используемого подшаблона могут использоваться переменные, после вставки текста в шаблон они также будут заменены.

В качестве значения переменной должен передаваться либо полный путь до вставляемого файла, либо относительный к текущей форме.

Выражение может быть дополнено параметрами: <\~variable\[?pageBreakBefore]\[?pageBreakAfter]\~>, где:

* pageBreakBefore - вставить символ переноса на новую страницу перед текстом подшаблона;
* pageBreakAfter - вставить символ переноса на новую страницу после текста подшаблона.

### <@PATH@> <a href="#variable_image" id="variable_image"></a>

Служит для вставки изображения.

Например, для вставки изображения с параметризованным путем следует указать выражения вида <@<#variable#>@> - для скалярных значений и <@<%variable%>@> - для массивов.

Выражение PATH имеет следующий формат: PATH\[?width=INT]\[?height=INT]\[?mode=MODE], где:

* PATH - полный путь до файла изображения;
* width - необязательный параметр ширины изображения; в качестве значения INT ожидается положительное целочисленное значение;
* height - необязательный параметр высоты изображения; в качестве значения INT ожидается положительное целочисленное значение;
* mode - необязательный параметр типа размера; в качестве значения MODE ожидается [тип размера изображения](export_to_doc_command.md#image_mode_types) (по умолчанию "Zoom").

#### Типы размера изображения <a href="#image_mode_types" id="image_mode_types"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="469.3333333333333"></th></tr></thead><tbody><tr><td align="center">Zoom</td><td>Растягивание изображения до указанной ширины и высоты (в большую или меньшую сторону), сохраняя пропорции изображения</td></tr><tr><td align="center">ZoomLess</td><td>Растягивание изображения до указанной ширины и высоты (только в меньшую сторону), сохраняя пропорции изображения</td></tr><tr><td align="center">Stretch</td><td>Растягивание изображения до указанной ширины и высоты без сохранения пропорций изображения</td></tr></tbody></table>

## Шаблон ExportToDocCommand <a href="#template_export_to_doc_command" id="template_export_to_doc_command"></a>

```xml
<Command Name="" Type="ExportToDocCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для ExportToDocCommand-->
  <Async Value="" />
  <TemplateFileName></TemplateFileName>
  <SaveFormattingInTables Value="" />
  <Parameters>
    <Parameter Name=""></Parameter>
  </Parameters>
  <Open></Open>
  <Print></Print>
  <PrintCopy></PrintCopy>
  <GroupTags SingleFile=""></GroupTags>
  <ExportFileName Ask=""></ExportFileName>
  <InsertPictures Value="" />
  <UseRawTags Value="" />
</Command>
```

## Описание ExportToDocCommand <a href="#description_export_to_doc_command" id="description_export_to_doc_command"></a>

```xml
<Command Name="ExportToDocCommandName" Type="ExportToDocCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для ExportToDocCommand-->
</Command>
```

### Результат выполнения ExportToDocCommand <a href="#result_export_to_doc_command" id="result_export_to_doc_command"></a>

#### Value <a href="#result_value" id="result_value"></a>

Полный путь с названием файла, который будет сгенерирован из указанного шаблона с подстановкой данных.

## Тэги, специфичные для ExportToDocCommand <a href="#tags_export_to_doc_command" id="tags_export_to_doc_command"></a>

### Async <a href="#async" id="async"></a>

Признак, определяющий, будет ли выполнение команды происходить в асинхронном режиме (в фоновом потоке).

Необязательный тэг. Значение тэга `<Async>`: не ожидается.

Если тэг `<Async>` отсутствует, то для атрибута `Value` используется значение False.

```xml
<Async Value="False" />
```

#### Атрибуты тэга `<Async>` <a href="#attributes_tag_async" id="attributes_tag_async"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

### TemplateFileName <a href="#template_file_name" id="template_file_name"></a>

Путь до DOC-файла шаблона.

Обязательный тэг. Любое значение будет переведено в текстовое.

Поддерживаются [константы замены](../values/replacement_constants.md).

```xml
<TemplateFileName>TemplateFileName.doc</TemplateFileName>
```

### SaveFormattingInTables <a href="#save_formatting_in_tables" id="save_formatting_in_tables"></a>

Признак, определяющий, будет ли в сформированных DOC-файлах сохраняться форматирование для текста, замененного из параметров-массивов и расположенного в таблицах.

Необязательный тэг. Значение тэга `<SaveFormattingInTables>`: не ожидается.

Если тэг `<SaveFormattingInTables>` отсутствует, то для атрибута `Value` используется значение False.

```xml
<SaveFormattingInTables Value="False" />
```

{% hint style="warning" %}
При сохранении форматирования текста, замененного из параметров-массивов и расположенного в таблицах, время формирования DOC-файлов может увеличиться в несколько раз.
{% endhint %}

#### Атрибуты тэга `<SaveFormattingInTables>` <a href="#attributes_tag_save_formatting_in_tables" id="attributes_tag_save_formatting_in_tables"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

### Parameters <a href="#parameters" id="parameters"></a>

Параметры, которые будут переданы в файл шаблона для замены.

Необязательный тэг. Значение тэга `<Parameters>`: список тэгов [`<Parameter>`](export_to_doc_command.md#parameters_parameter).

```xml
<Parameters>
  <Parameter Name="ParameterName1">ParameterValue1</Parameter>
  <Parameter Name="ParameterName2">ParameterValue2</Parameter>
</Parameters>
```

#### Тэг `<Parameter>` <a href="#parameters_parameter" id="parameters_parameter"></a>

Параметр, который будет передан в файл шаблона для замены.

Необязательный тэг. Значение тэга `<Parameter>`: любое значение.

#### Атрибуты тэга `<Parameter>` <a href="#attributes_tag_parameters_parameter" id="attributes_tag_parameters_parameter"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название параметра.</p><p></p><p>Обязательный атрибут. Значение атрибута <code>Name</code>: название одной из <a href="export_to_doc_command.md#supported_variables">переменных</a>, использующихся в файле шаблона.</p><p></p><p>Переменные в шаблоне задаются как &#x3C;#ParameterName1#> - для отображения скалярного значения или &#x3C;%ParameterName1%> - для отображения массива при использовании в таблице.</p></td></tr></tbody></table>

### Open <a href="#open" id="open"></a>

Признак открытия DOC-файла после формирования.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение True.

```xml
<Open>True</Open>
```

### Print <a href="#print" id="print"></a>

Признак печати DOC-файла после формирования.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<Print>False</Print>
```

### PrintCopy <a href="#print_copy" id="print_copy"></a>

Количество копий для печати DOC-файла после формирования.

Необязательный тэг. Ожидается положительное целочисленное значение.

По умолчанию используется значение 1.&#x20;

```xml
<PrintCopy>1</PrintCopy>
```

### GroupTags <a href="#group_tags" id="group_tags"></a>

Группировочные признаки параметров (экспорт в несколько файлов одновременно).

Необязательный тэг. Ожидается линейный массив значений.

По умолчанию экспорт происходит только в 1 файл.

```xml
<GroupTags SingleFile="False"></GroupTags>
```

Необязательный атрибут `SingleFile` - признак, определяющий, будут ли экспортируемые файлы объединены в один документ.

Ожидается логическое значение.

По умолчанию используется значение False.

#### Пример <a href="#example_group_tags" id="example_group_tags"></a>

Значение тэга `<GroupTags>` - массив некоторых значений: "Значение A; Значение B; Значение C". Это уже означает, что будет создано 3 DOC-файла (по количеству значений в массиве `<GroupTags>`). Нужно только распределить значения параметров по этим файлам. Правила распределения следующие:

1\. Если параметр представляет собой матрицу значений, то первый ее столбец будет использоваться как указание на то, к какому файлу следует соотнести значение из второго столбца.

Например, рассмотрим в качестве значения параметра "Prm1" следующую матрицу:

<table data-header-hidden><thead><tr><th width="364.21182266009856" align="center"></th><th width="363" align="center"></th></tr></thead><tbody><tr><td align="center">Значение A</td><td align="center">Значение A1</td></tr><tr><td align="center">Значение B</td><td align="center">Значение B1</td></tr><tr><td align="center">Значение B</td><td align="center">Значение B2</td></tr><tr><td align="center">Значение C</td><td align="center">Значение C1</td></tr><tr><td align="center">Значение D</td><td align="center">Значение D1</td></tr></tbody></table>

В соответствии с этим правилом, для выгружаемого файла, соответствующему группировочному признаку "Значение A", значение параметра "Prm1" будет "Значение A1"; для файла "Значение B" - массив значений "Значение B1; Значение B2"; для файла "Значение C" - "Значение C1". Последняя строка матрицы "Значение D; Значение D1" не будет адресована ни в один файл, т.к. значение в первом столбце не соответствует ни одному из группировочных значений.

2\. Если параметр не является матрицей (массив или скалярное значение), то данный параметр будет адресован во все создаваемые файлы без изменений.

### ExportFileName <a href="#export_file_name" id="export_file_name"></a>

Полный путь до PDF-файла, в который будут выгружены данные.

Необязательный тэг. Любое значение будет переведено в текстовое.

Если тэг `<ExportFileName>` отсутствует, то имя файла выбирается произвольно в системной папке Temp.

Поддерживаются [константы замены](../values/replacement_constants.md).

```xml
<ExportFileName Ask="False">ExportFileName</ExportFileName>
```

Необязательный атрибут `Ask`  - признак, определяющий, будет ли задан вопрос о пути экспорта PDF-файла.

Ожидается логическое значение.

По умолчанию используется значение False.

### InsertPictures <a href="#insert_pictures" id="insert_pictures"></a>

Признак, определяющий, будет ли выполнена замена в файле шаблона тэгов вставки изображений.

Необязательный тэг. Значение тэга не ожидается. Обязательный атрибут `Value` ожидает логическое значение.

По умолчанию используется значение True.

Если атрибут `Value` имеет значение False, то замена в файле шаблона тэгов вставки изображений не произойдет и тэги останутся без изменений.

```xml
<InsertPictures Value="" />
```

### UseRawTags <a href="#use_raw_tags" id="use_raw_tags"></a>

Признак, определяющий, будет ли выполнена замена в файле шаблона тэгов вставки скалярных, табличных значений и изображений.

Необязательный тэг. Значение тэга не ожидается. Обязательный атрибут `Value` ожидает логическое значение.

По умолчанию используется значение False.

Если атрибут `Value` имеет значение True, то замена в файле шаблона тэгов вставки скалярных и табличных значений и изображений не произойдет и тэги останутся без изменений.

```xml
<UseRawTags Value="" />
```
