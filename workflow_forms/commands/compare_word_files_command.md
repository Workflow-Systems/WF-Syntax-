---
description: Команда; сравнивает 2 файла Microsoft Word.
---

# CompareWordFilesCommand

## Шаблон CompareWordFilesCommand <a href="#template" id="template"></a>

```xml
<Command Name="" Type="CompareWordFilesCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для CompareWordFilesCommand-->
  <File1></File1>
  <File2></File2>
</Command>
```

## Описание CompareWordFilesCommand <a href="#description" id="description"></a>

```xml
<Command Name="CompareWordFilesCommandName" Type="CompareWordFilesCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для CompareWordFilesCommand-->
</Command>
```

### Результат выполнения CompareWordFilesCommand <a href="#result" id="result"></a>

Команда не имеет результата.

## Тэги, специфичные для CompareWordFilesCommand <a href="#specific-tags" id="specific-tags"></a>

### File1 <a href="#file1" id="file1"></a>

Путь до первого файла для сравнения.

Обязательный тэг. Любое значение будет переведено в текстовое.

Поддерживаются [константы замены](../values/replacement_constants.md).

```xml
<File1>FullPath\\FileName.ext</File1>
```

### File2 <a href="#file2" id="file2"></a>

Путь до второго файла для сравнения.

Обязательный тэг. Любое значение будет переведено в текстовое.

Поддерживаются [константы замены](../values/replacement_constants.md).

```xml
<File2>FullPath\\FileName.ext</File2>
```
