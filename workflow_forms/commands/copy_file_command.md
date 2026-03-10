---
description: Команда; копирует файлы.
---

# CopyFileCommand

## Шаблон CopyFileCommand <a href="#template" id="template"></a>

```xml
<Command Name="" Type="CopyFileCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для CopyFileCommand-->
  <Async Value="" />
  <FilesToCopy></FilesToCopy>
  <ExportFileName Ask=""></ExportFileName>
</Command>
```

## Описание CopyFileCommand <a href="#description" id="description"></a>

```xml
<Command Name="CopyFileCommandName" Type="CopyFileCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для CopyFileCommand-->
</Command>
```

### Результат выполнения CopyFileCommand <a href="#result" id="result"></a>

#### Value <a href="#result_value" id="result_value"></a>

Список путей для скопированных файлов.

#### ErrorMessage <a href="#result_error_message" id="result_error_message"></a>

Сообщение об ошибках.

Если ошибок не было, то значение будет null.

#### IsError <a href="#result_is_error" id="result_is_error"></a>

Признак того, были ли ошибки при выполнении команды.

## Тэги, специфичные для CopyFileCommand <a href="#specific-tags" id="specific-tags"></a>

### Async <a href="#async" id="async"></a>

Признак, определяющий, будет ли выполнение команды происходить в асинхронном режиме (в фоновом потоке).

Необязательный тэг. Значение тэга не ожидается.\
Обязательный атрибут `Value` ожидает логическое значение

По умолчанию используется значение False.

```xml
<Async Value="False" />
```

### FilesToCopy <a href="#files_to_copy" id="files_to_copy"></a>

Список путей до файлов, которые будут скопированы.

Обязательный тэг. Любое значение будет переведено в массив текстовых значений.

Поддерживаются [константы замены](../values/replacement_constants.md).

```xml
<FilesToCopy></FilesToCopy>
```

### ExportFileName <a href="#export_file_name" id="export_file_name"></a>

Путь для копирования файлов.

Обязательный тэг. Любое значение будет переведено в массив текстовых значений.

Если указан путь с расширением, то файлы будут переименованы.

Если в тэге [`<FilesToCopy>`](copy_file_command.md#files_to_copy) больше одного пути, то в тэге `<ExportFileName>` ожидается путь до папки куда будут скопированы файлы либо массив путей того же размера, что и в тэге [`<FilesToCopy>`](copy_file_command.md#files_to_copy).

В массиве может быть либо папка, либо путь до файла. Если это папка, то произойдёт простое копирование, если путь до файла - файл будет скопирован с указанным именем.

Поддерживаются [константы замены](../values/replacement_constants.md).

```xml
<ExportFileName Ask="False">ExportFileName</ExportFileName>
```

#### Атрибуты тэга `<ExportFileName>` <a href="#attributes_tag_export_file_name" id="attributes_tag_export_file_name"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="476.3333333333333"></th></tr></thead><tbody><tr><td align="center">Ask</td><td><p>Признак, определяющий, будет ли задан вопрос о пути сохранения файлов, если существует файл с таким же именем в папке назначения.</p><p></p><p>Необязательный атрибут. Ожидается логическое значение.</p><p></p><p>Если атрибут <code>Ask</code> отсутствует, то используется значение False.</p><p></p><p>Если атрибут <code>Ask</code> отсутствует, в случае если в папке назначения существует файл с совпадающем именем, то происходит автоматическое переименование файла с индексом.</p></td></tr></tbody></table>
