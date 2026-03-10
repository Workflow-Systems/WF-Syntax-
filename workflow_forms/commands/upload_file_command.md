---
description: Команда; отправляет файлы на сервер.
---

# UploadFileCommand

## Шаблон UploadFileCommand <a href="#template_upload_file_command" id="template_upload_file_command"></a>

```xml
<Command Name="" Type="UploadFileCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для UploadFileCommand-->
  <Async Value="" />
  <FileName></FileName>
  <Storage></Storage>
</Command>
```

## Описание UploadFileCommand <a href="#description_upload_file_command" id="description_upload_file_command"></a>

```xml
<Command Name="UploadFileCommandName" Type="UploadFileCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для UploadFileCommand-->
</Command>
```

### Результат выполнения UploadFileCommand <a href="#result_upload_file_command" id="result_upload_file_command"></a>

#### Value <a href="#result_value" id="result_value"></a>

Сгенерированные на сервере guid-идентификаторы отправленных файлов.

## Тэги, специфичные для UploadFileCommand <a href="#tags_upload_file_command" id="tags_upload_file_command"></a>

### Async <a href="#async" id="async"></a>

Признак, определяющий, будет ли выполнение команды происходить в асинхронном режиме (в фоновом потоке).

Необязательный тэг. Значение тэга не ожидается.\
Обязательный атрибут `Value` ожидает логическое значение

По умолчанию используется значение False.

```xml
<Async Value="False" />
```

### FileName <a href="#file_name" id="file_name"></a>

Полный путь до файлов, которые будут отправлены на сервер.

Обязательный тэг. Любое значение будет переведено в массив текстовых значений.

Поддерживаются [константы замены](../values/replacement_constants.md).

```xml
<FileName>FullPath\\FileName.ext</FileName>
```

### Storage <a href="#storage" id="storage"></a>

Название хранилища на сервере, куда будет записан файл.

Необязательный тэг. Любое значение будет переведено в текстовое.

Если хранилище не указано, то файл будет записан в хранилище с именем Default.

```xml
<Storage>Default</Storage>
```
