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

Необязательный тэг. Значение тэга `<Async>`: не ожидается.

Если тэг `<Async>` отсутствует, то для атрибута `Value` используется значение False.

```xml
<Async Value="False" />
```

#### Атрибуты тэга `<Async>` <a href="#attributes_tag_async" id="attributes_tag_async"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

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
