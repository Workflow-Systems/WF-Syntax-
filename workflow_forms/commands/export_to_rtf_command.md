---
description: >-
  Команда; генерирует RTF-файл из шаблона, в котором вместо переменных
  подставляются определенные значения.
---

# ExportToRtfCommand

## Поддерживаемые переменные <a href="#supported_variables" id="supported_variables"></a>

### <#variable#> <a href="#variable_scalar" id="variable_scalar"></a>

Служит для отображения скалярного значения.

### <%variable%> <a href="#variable_array" id="variable_array"></a>

Служит для отображения массива (для использования в таблице).

## Шаблон ExportToRtfCommand <a href="#template_export_to_rtf_command" id="template_export_to_rtf_command"></a>

```xml
<Command Name="" Type="ExportToRtfCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для ExportToRtfCommand-->
  <Async Value="" />
  <TemplateFileName></TemplateFileName>
  <ReturnCode></ReturnCode>
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

## Описание ExportToRtfCommand <a href="#description_export_to_rtf_command" id="description_export_to_rtf_command"></a>

```xml
<Command Name="ExportToRtfCommandName" Type="ExportToRtfCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для ExportToRtfCommand-->
</Command>
```

### Результат выполнения ExportToRtfCommand <a href="#result_export_to_rtf_command" id="result_export_to_rtf_command"></a>

#### Value <a href="#result_value" id="result_value"></a>

Полный путь с названием файла, который будет сгенерирован из указанного шаблона с подстановкой данных.

## Тэги, специфичные для ExportToRtfCommand <a href="#tags_export_to_rtf_command" id="tags_export_to_rtf_command"></a>

### Async <a href="#async" id="async"></a>

Признак, определяющий, будет ли выполнение команды происходить в асинхронном режиме (в фоновом потоке).

Необязательный тэг. Значение тэга не ожидается.\
Обязательный атрибут `Value` ожидает логическое значение

По умолчанию используется значение False.

```xml
<Async Value="False" />
```

### TemplateFileName <a href="#template_file_name" id="template_file_name"></a>

Путь до RTF-файла шаблона.

Обязательный тэг. Любое значение будет переведено в текстовое.

Поддерживаются [константы замены](../values/replacement_constants.md).

```xml
<TemplateFileName>TemplateFileName.rtf</TemplateFileName>
```

### ReturnCode <a href="#return_code" id="return_code"></a>

Текст, который будет интерпретироваться как перенос на новую строку в экспортируемом файле.

Необязательный тэг. Любое значение будет переведено в текстовое.

Если тэг `<ReturnCode>` отсутствует, то перенос на новую строку в экспортируемом файле производиться не будет.

```xml
<ReturnCode>\RETURN_CODE</ReturnCode>
```

### Parameters <a href="#parameters" id="parameters"></a>

Параметры, которые будут переданы в файл шаблона для замены.

Необязательный тэг. Значение тэга `<Parameters>`: список тэгов [`<Parameter>`](export_to_rtf_command.md#parameters_parameter).

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

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название параметра.</p><p></p><p>Обязательный атрибут. Значение атрибута <code>Name</code>: название одной из <a href="export_to_rtf_command.md#supported_variables">переменных</a>, использующихся в файле шаблона.</p><p></p><p>Переменные в шаблоне задаются как &#x3C;#ParameterName1#> - для отображения скалярного значения или &#x3C;%ParameterName1%> - для отображения массива при использовании в таблице.</p></td></tr></tbody></table>

### Open <a href="#open" id="open"></a>

Признак открытия RTF-файла после формирования.

Необязательный тэг. Ожидается логическое значение.

Если тэг `<Open>` отсутствует, то используется значение True.

```xml
<Open>True</Open>
```

### Print <a href="#print" id="print"></a>

Признак печати RTF-файла после формирования.

Необязательный тэг. Ожидается логическое значение.

Если тэг `<Print>` отсутствует, то используется значение False.

```xml
<Print>False</Print>
```

### PrintCopy <a href="#print_copy" id="print_copy"></a>

Количество копий для печати RTF-файла после формирования.

Необязательный тэг. Ожидается положительное целочисленное значение.

Если тэг `<PrintCopy>` отсутствует, то используется значение 1.&#x20;

```xml
<PrintCopy>1</PrintCopy>
```

### GroupTags <a href="#group_tags" id="group_tags"></a>

Группировочные признаки параметров (экспорт в несколько файлов одновременно).

Необязательный тэг. Ожидается линейный массив значений.

Если тэг `<GroupTags>` отсутствует, то экспорт происходит только в 1 файл.

```xml
<GroupTags SingleFile="False"></GroupTags>
```

#### Атрибуты тэга `<GroupTags>` <a href="#attributes_tag_group_tags" id="attributes_tag_group_tags"></a>

<table data-header-hidden><thead><tr><th width="228.6296484971982" align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">SingleFile</td><td><p>Признак, определяющий, будут ли экспортируемые файлы объединены в один документ.</p><p></p><p>Необязательный атрибут. Ожидается логическое значение.</p><p></p><p>Если атрибут <code>SingleFile</code> отсутствует, то используется значение False.</p></td></tr></tbody></table>

#### Пример <a href="#example_group_tags" id="example_group_tags"></a>

Значение тэга `<GroupTags>` - массив некоторых значений: "Значение A; Значение B; Значение C". Это уже означает, что будет создано 3 RTF-файла (по количеству значений в массиве `<GroupTags>`). Нужно только распределить значения параметров по этим файлам. Правила распределения следующие:

1\. Если параметр представляет собой матрицу значений, то первый ее столбец будет использоваться как указание на то, к какому файлу следует соотнести значение из второго столбца.

Например, рассмотрим в качестве значения параметра "Prm1" следующую матрицу:

<table data-header-hidden><thead><tr><th width="364.21182266009856" align="center"></th><th width="363" align="center"></th></tr></thead><tbody><tr><td align="center">Значение A</td><td align="center">Значение A1</td></tr><tr><td align="center">Значение B</td><td align="center">Значение B1</td></tr><tr><td align="center">Значение B</td><td align="center">Значение B2</td></tr><tr><td align="center">Значение C</td><td align="center">Значение C1</td></tr><tr><td align="center">Значение D</td><td align="center">Значение D1</td></tr></tbody></table>

В соответствии с этим правилом, для выгружаемого файла, соответствующему группировочному признаку "Значение A", значение параметра "Prm1" будет "Значение A1"; для файла "Значение B" - массив значений "Значение B1; Значение B2"; для файла "Значение C" - "Значение C1". Последняя строка матрицы "Значение D; Значение D1" не будет адресована ни в один файл, т.к. значение в первом столбце не соответствует ни одному из группировочных значений.

2\. Если параметр не является матрицей (массив или скалярное значение), то данный параметр будет адресован во все создаваемые файлы без изменений.

### ExportFileName <a href="#export_file_name" id="export_file_name"></a>

Полный путь до RTF-файла, в который будут выгружены данные.

Необязательный тэг. Любое значение будет переведено в текстовое.

Если тэг `<ExportFileName>` отсутствует, то имя файла выбирается произвольно в системной папке Temp.

Поддерживаются [константы замены](../values/replacement_constants.md).

```xml
<ExportFileName Ask="False">ExportFileName</ExportFileName>
```

#### Атрибуты тэга `<ExportFileName>` <a href="#attributes_tag_export_file_name" id="attributes_tag_export_file_name"></a>

<table data-header-hidden><thead><tr><th width="228.6296484971982" align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Ask</td><td><p>Признак, определяющий, будет ли задан вопрос о пути экспорта RTF-файла.</p><p></p><p>Необязательный атрибут. Ожидается логическое значение.</p><p></p><p>Если атрибут <code>Ask</code> отсутствует, то используется значение False.</p></td></tr></tbody></table>

### InsertPictures <a href="#insert_pictures" id="insert_pictures"></a>

Признак, определяющий, будет ли выполнена замена в файле шаблона тэгов вставки изображений.

Необязательный тэг. Значение тэга `<InsertPictures>`: не ожидается.

Если тэг `<InsertPictures>` отсутствует, то для атрибута `Value` используется значение True.

Если атрибут `Value` в тэге `<InsertPictures>` имеет значение False, то замена в файле шаблона тэгов вставки изображений не произойдет и тэги останутся без изменений.

```xml
<InsertPictures Value="" />
```

#### Атрибуты тэга `<InsertPictures>` <a href="#attributes_tag_insert_pictures" id="attributes_tag_insert_pictures"></a>

<table data-header-hidden><thead><tr><th width="228.6296484971982" align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

### UseRawTags <a href="#use_raw_tags" id="use_raw_tags"></a>

Признак, определяющий, будет ли выполнена замена в файле шаблона тэгов вставки скалярных, табличных значений и изображений.

Необязательный тэг. Значение тэга `<UseRawTags>`: не ожидается.

Если тэг `<UseRawTags>` отсутствует, то для атрибута `Value` используется значение False.

Если атрибут `Value` в тэге `<UseRawTags>` имеет значение True, то замена в файле шаблона тэгов вставки скалярных и табличных значений и изображений не произойдет и тэги останутся без изменений.

```xml
<UseRawTags Value="" />
```

#### Атрибуты тэга `<UseRawTags>` <a href="#attributes_tag_use_raw_tags" id="attributes_tag_use_raw_tags"></a>

<table data-header-hidden><thead><tr><th width="231.32842626519306" align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>
