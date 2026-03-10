---
description: Команда; заменяет файлы на сервере.
---

# ReplaceFileCommand

## Шаблон ReplaceFileCommand <a href="#template_replace_file_command" id="template_replace_file_command"></a>

```xml
<Command Name="" Type="ReplaceFileCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для ReplaceFileCommand-->
  <Async Value="" />
  <FileName></FileName>
  <FileGuid></FileGuid>
</Command>
```

## Описание ReplaceFileCommand <a href="#description_replace_file_command" id="description_replace_file_command"></a>

```xml
<Command Name="ReplaceFileCommandName" Type="ReplaceFileCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для ReplaceFileCommand-->
</Command>
```

### Результаты выполнения ReplaceFileCommand <a href="#result_replace_file_command" id="result_replace_file_command"></a>

Команда результата не имеет.

## Тэги, специфичные для ReplaceFileCommand <a href="#tags_replace_file_command" id="tags_replace_file_command"></a>

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

### FileGuid <a href="#file_guid" id="file_guid"></a>

Guid'ы файлов на сервере.

Обязательный тэг. Любое значение будет переведено в массив текстовых значений.

```xml
<FileGuid>Guid</FileGuid>
```
