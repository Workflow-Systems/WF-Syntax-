---
description: Команда; генерирует PDF-файл на основе шаблона формата RTF, DOC или DOCX.
---

# ConvertDocumentToPdfCommand

## Шаблон ConvertDocumentToPdfCommand <a href="#template" id="template"></a>

```xml
<Command Name="" Type="ConvertDocumentToPdfCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для ConvertDocumentToPdfCommand-->
  <Async Value="" />
  <TemplateFileName></TemplateFileName>
  <Open></Open>
  <Print></Print>
  <PrintCopy></PrintCopy>
  <ExportFileName Ask=""></ExportFileName>
</Command>
```

## Описание ConvertDocumentToPdfCommand <a href="#description" id="description"></a>

```xml
<Command Name="ConvertDocumentToPdfCommandName" Type="ConvertDocumentToPdfCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для ConvertDocumentToPdfCommand-->
</Command>
```

### Результат выполнения ConvertDocumentToPdfCommand <a href="#result" id="result"></a>

#### Value <a href="#result_value" id="result_value"></a>

Полный путь с названием файла, который будет сгенерирован из указанного шаблона с подстановкой данных.

## Тэги, специфичные для ConvertDocumentToPdfCommand <a href="#specific-tags" id="specific-tags"></a>

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

Путь до файла шаблона. Поддерживаются форматы .rtf, .doc и .docx.

Обязательный тэг. Любое значение будет переведено в текстовое.

Поддерживаются [константы замены](../values/replacement_constants.md).

```xml
<TemplateFileName>TemplateFileName.doc</TemplateFileName>
```

### Open <a href="#open" id="open"></a>

Признак открытия PDF-файла после формирования.

Необязательный тэг. Ожидается логическое значение.

Если тэг `<Open>` отсутствует, то используется значение True.

```xml
<Open>True</Open>
```

### Print <a href="#print" id="print"></a>

Признак печати PDF-файла после формирования.

Необязательный тэг. Ожидается логическое значение.

Если тэг `<Print>` отсутствует, то используется значение False.

```xml
<Print>False</Print>
```

### PrintCopy <a href="#print_copy" id="print_copy"></a>

Количество копий для печати PDF-файла после формирования.

Необязательный тэг. Ожидается положительное целочисленное значение.

Если тэг `<PrintCopy>` отсутствует, то используется значение 1.

```xml
<PrintCopy>1</PrintCopy>
```

### ExportFileName <a href="#export_file_name" id="export_file_name"></a>

Полный путь до PDF-файла, в который будут выгружены данные.

Необязательный тэг. Любое значение будет переведено в текстовое.

Если тэг `<ExportFileName>` отсутствует, то имя файла выбирается произвольно в системной папке Temp.

Поддерживаются [константы замены](../values/replacement_constants.md).

```xml
<ExportFileName Ask="False">ExportFileName</ExportFileName>
```

#### Атрибуты тэга `<ExportFileName>` <a href="#attributes_tag_export_file_name" id="attributes_tag_export_file_name"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Ask</td><td><p>Признак, определяющий, будет ли задан вопрос о пути экспорта PDF-файла.</p><p></p><p>Необязательный атрибут. Ожидается логическое значение.</p><p></p><p>Если атрибут <code>Ask</code> отсутствует, то используется значение False.</p></td></tr></tbody></table>
