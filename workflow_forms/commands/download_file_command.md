---
description: Команда; получает файлы с сервера или из интернета.
---

# DownloadFileCommand

## Шаблон DownloadFileCommand <a href="#template_download_file_command" id="template_download_file_command"></a>

```xml
<Command Name="" Type="DownloadFileCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для DownloadFileCommand-->
  <Async Value="" />
  <FileGuid></FileGuid>
  <FileUrl></FileUrl>
  <Open></Open>
  <Print></Print>
  <ReadOnly></ReadOnly>
  <ExportFileName Ask=""></ExportFileName>
  <AllowOverwrite></AllowOverwrite>
</Command>
```

## Описание DownloadFileCommand <a href="#description_download_file_command" id="description_download_file_command"></a>

```xml
<Command Name="DownloadFileCommandName" Type="DownloadFileCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для DownloadFileCommand-->
</Command>
```

### Результат выполнения DownloadFileCommand <a href="#result_download_file_command" id="result_download_file_command"></a>

#### Value <a href="#result_value" id="result_value"></a>

Линейный массив полных путей с названиями загруженных файлов.

## Тэги, специфичные для DownloadFileCommand <a href="#tags_download_file_command" id="tags_download_file_command"></a>

### Async <a href="#async" id="async"></a>

Признак, определяющий, будет ли выполнение команды происходить в асинхронном режиме (в фоновом потоке).

Необязательный тэг. Значение тэга не ожидается.\
Обязательный атрибут `Value` ожидает логическое значение

По умолчанию используется значение False.

```xml
<Async Value="False" />
```

### FileGuid <a href="#file_guid" id="file_guid"></a>

Guid'ы файлов на сервере.

Необязательный тэг.  Любое значение будет переведено в массив текстовых значений.

При наличии тэга `<FileGuid>` поле [`<FileUrl>`](download_file_command.md#file_url) игнорируется, однако при его отсутствии тэг [`<FileUrl>`](download_file_command.md#file_url) обязателен.

```xml
<FileGuid>Guid</FileGuid>
```

### FileUrl <a href="#file_url" id="file_url"></a>

URL'ы файлов в интернете.

Необязательный тэг. Любое значение будет переведено в массив текстовых значений.

Игнорируется при наличии тэга [`<FileGuid>`](download_file_command.md#file_guid).

```xml
<FileUrl>Ссылка</FileUrl>
```

### Open <a href="#open" id="open"></a>

Признак, определяющий, следует ли открывать загруженные файлы.

Необязательный тэг. Ожидается логическое значение.

Если тэг `<Open>` отсутствует, то используется значение True.

Если тэг `<Open>` отсутствует, но присутствует тэг [`<Print>`](download_file_command.md#print), то используется значение False.

```xml
<Open>True</Open>
```

### Print <a href="#print" id="print"></a>

Признак, определяющий, следует ли печатать загруженные файлы.

Необязательный тэг. Ожидается логическое значение.

Если тэг `<Print>` отсутствует, то используется значение False.

```xml
<Print>False</Print>
```

### ReadOnly <a href="#read_only" id="read_only"></a>

Признак, определяющий, будут ли загруженные файлы иметь признак "Только для чтения".

Необязательный тэг. Ожидается логическое значение.

Если тэг `<ReadOnly>` отсутствует, то используется значение True.

```xml
<ReadOnly>True</ReadOnly>
```

### AllowOverwrite <a href="#allow_overwrite" id="allow_overwrite"></a>

Признак, определяющий, будет ли в момент загрузки автоматически перезаписан файл, при условии, что его имя совпадает с уже существующим файлом.

Необязательный тэг. Ожидается логическое значение.

Если тэг отсутствует, то используется значение False.

```xml
<AllowOverwrite>True</AllowOverwrite>
```

### ExportFileName <a href="#export_file_name" id="export_file_name"></a>

Полный путь, по которому будут сохранены выгруженные файлы.

Необязательный тэг. Любое значение будет переведено в текстовое.

Если тэг `<ExportFileName>` отсутствует, то имена файлов выбираются произвольно во временной папке Temp профиля пользователя.

Поддерживаются [константы замены](../values/replacement_constants.md).

```xml
<ExportFileName Ask="False">ExportFileName</ExportFileName>
```

#### Атрибуты тэга `<ExportFileName>` <a href="#attributes_tag_export_file_name" id="attributes_tag_export_file_name"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="476.3333333333333"></th></tr></thead><tbody><tr><td align="center">Ask</td><td><p>Признак, определяющий, будет ли задан вопрос о пути сохранения файлов.</p><p></p><p>Необязательный атрибут. Ожидается логическое значение.</p><p></p><p>Если атрибут <code>Ask</code> отсутствует, то используется значение False.</p></td></tr></tbody></table>
