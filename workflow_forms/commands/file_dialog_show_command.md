---
description: Команда; открывает диалоговое окно выбора файла.
---

# FileDialogShowCommand

## Шаблон FileDialogShowCommand <a href="#template_file_dialog_show_command" id="template_file_dialog_show_command"></a>

```xml
<Command Name="" Type="FileDialogShowCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для FileDialogShowCommand-->
  <Type Value="" />
  <Title></Title>
  <InitialDirectory></InitialDirectory>
  <Filter></Filter>
  <FilterIndex></FilterIndex>
  <MultiSelect></MultiSelect>
</Command>
```

## Описание FileDialogShowCommand <a href="#description_file_dialog_show_command" id="description_file_dialog_show_command"></a>

```xml
<Command Name="FileDialogShowCommandName" Type="FileDialogShowCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для FileDialogShowCommand-->
</Command>
```

### Результат выполнения FileDialogShowCommand <a href="#result_file_dialog_show_command" id="result_file_dialog_show_command"></a>

#### OK <a href="#result_ok" id="result_ok"></a>

Признак того, что в диалоговом окне пользователем был выбран хотя бы 1 файл.

#### Path <a href="#result_path" id="result_path"></a>

Массив путей до папок, в который расположены выбранные файлы, или путь до папки, в котором расположен 1 выбранный файл.

#### FileName <a href="#result_file_name" id="result_file_name"></a>

Массив имен выбранных файлов (только имена, без расширения), или имя 1 выбранного файла.

#### FileNameExtension <a href="#result_file_name_extension" id="result_file_name_extension"></a>

Массив расширений выбранных файлов (с точкой в начале), или расширение 1 выбранного файла.

#### FullFileName <a href="#result_full_file_name" id="result_full_file_name"></a>

Массив полных имен выбранных файлов (имя и расширение), или полное имя 1 выбранного файла.

#### FullPath <a href="#result_full_path" id="result_full_path"></a>

Массив полных путей до выбранных файлов (путь и полное имя), или полный путь до 1 выбранного файла.

## Тэги, специфичные для FileDialogShowCommand <a href="#tags_file_dialog_show_command" id="tags_file_dialog_show_command"></a>

### Type <a href="#type" id="type"></a>

Тип диалогового окна, открываемого командой.

Необязательный тэг. Значение тэга `<Type>`: не ожидается.

Если тэг `<Type>` отсутствует, то для атрибута `Value` используется значение Open.

```xml
<Type Value="Open" />
```

#### Атрибуты тэга `<Type>` <a href="#attributes_tag_type" id="attributes_tag_type"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="469.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Название типа диалогового окна.</p><p></p><p>Обязательный атрибут. Ожидается название одного из <a href="file_dialog_show_command.md#dialog_box_types">типов диалогового окна</a>.</p></td></tr></tbody></table>

#### Типы диалогового окна <a href="#dialog_box_types" id="dialog_box_types"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="469.3333333333333"></th></tr></thead><tbody><tr><td align="center">Open</td><td>Диалоговое окно для открытия файла</td></tr><tr><td align="center">Save</td><td>Диалоговое окно для сохранения файла</td></tr></tbody></table>

### Title <a href="#title" id="title"></a>

Заголовок диалогового окна.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Title>Title</Title>
```

### InitialDirectory <a href="#initial_directory" id="initial_directory"></a>

Путь до папки, с которой будет начат обзор.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<InitialDirectory>InitialDirectory</InitialDirectory>
```

### Filter <a href="#filter" id="filter"></a>

Список поддерживаемых расширений диалогового окна.

Необязательный тэг. Любое значение будет переведено в текстовое.

Пример значения тэга `<Filter>`: Word 2007 | \*.docx | Все файлы | \*.\*_._

```xml
<Filter>Filter</Filter>
```

### FilterIndex <a href="#filter_index" id="filter_index"></a>

Индекс расширения, которое будет установлено как расширение для обзора по умолчанию.

Необязательный тэг. Ожидается целочисленное значение (от 1).

```xml
<FilterIndex>1</FilterIndex>
```

### MultiSelect <a href="#multi_select" id="multi_select"></a>

Признак, определяющий, можно ли в диалоге выбора файлов выбрать несколько файлов.

Необязательный тэг. ожидается логическое значение.

Если тэг `<MultiSelect>` отсутствует, то используется значение False.

```xml
<MultiSelect>False</MultiSelect>
```
