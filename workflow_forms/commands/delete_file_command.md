---
description: Команда; удаляет файлы с сервера.
---

# DeleteFileCommand

## Шаблон DeleteFileCommand <a href="#template_delete_file_command" id="template_delete_file_command"></a>

```xml
<Command Name="" Type="DeleteFileCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для DeleteFileCommand-->
  <Async Value="" />
  <FileGuid></FileGuid>
  <ThrowException></ThrowException>
</Command>
```

## Описание DeleteFileCommand <a href="#description_delete_file_command" id="description_delete_file_command"></a>

```xml
<Command Name="DeleteFileCommandName" Type="DeleteFileCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для DeleteFileCommand-->
</Command>
```

### Результат выполнения DeleteFileCommand <a href="#result_delete_file_command" id="result_delete_file_command"></a>

Команда не имеет результата.

## Тэги, специфичные для DeleteFileCommand <a href="#tags_delete_file_command" id="tags_delete_file_command"></a>

### Async <a href="#async" id="async"></a>

Признак, определяющий, будет ли выполнение команды происходить в асинхронном режиме (в фоновом потоке).

Необязательный тэг. Значение тэга `<Async>`: не ожидается.

Если тэг `<Async>` отсутствует, то для атрибута `Value` используется значение False.

```xml
<Async Value="False" />
```

#### Атрибуты тэга `<Async>` <a href="#attributes_tag_async" id="attributes_tag_async"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

### FileGuid <a href="#file_guid" id="file_guid"></a>

Guid'ы файлов на сервере.

Обязательный тэг. Любое значение будет переведено в массив текстовых значений.

```xml
<FileGuid>Guid</FileGuid>
```

### ThrowException <a href="#throw_exception" id="throw_exception"></a>

Признак, определяющий, будут ли проигнорированы все ошибки при выполнении команды.

Необязательный тэг. Ожидается логическое значение.

Если тэг `<ThrowException>` отсутствует, то значение по умолчанию True. Если значение будет False, то ошибки будут проигнорированы.

```xml
<ThrowException></ThrowException>
```
