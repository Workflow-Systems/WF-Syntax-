---
description: Команда; сохраняет изображение из буфера обмена в файл.
---

# SaveClipboardImageCommand

## Шаблон SaveClipboardImageCommand <a href="#template_save_clipboard_image_command" id="template_save_clipboard_image_command"></a>

```xml
<Command Name="" Type="SaveClipboardImageCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для SaveClipboardImageCommand-->
  <ImageFormat></ImageFormat>
  <ExportFileName Ask=""></ExportFileName>
</Command>
```

## Описание SaveClipboardImageCommand <a href="#description_save_clipboard_image_command" id="description_save_clipboard_image_command"></a>

```xml
<Command Name="SaveClipboardImageCommandName" Type="SaveClipboardImageCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для SaveClipboardImageCommand-->
</Command>
```

### Результат выполнения SaveClipboardImageCommand <a href="#result_save_clipboard_image_command" id="result_save_clipboard_image_command"></a>

#### Value <a href="#result_value" id="result_value"></a>

Путь до файла с изображением.

## Тэги, специфичные для SaveClipboardImageCommand <a href="#tags_save_clipboard_image_command" id="tags_save_clipboard_image_command"></a>

### ImageFormat <a href="#image_format" id="image_format"></a>

Название [формата изображения](save_clipboard_image_command.md#image_formats) для сохранения.

Необязательный тэг. Ожидается название одного из форматов изображений.

Если тэг `<ImageFormat>` отсутствует, то используется значение Png.

#### Форматы изображений <a href="#image_formats" id="image_formats"></a>

1. Bmp
2. Gif
3. Jpg
4. Png
5. Tiff

```xml
<ImageFormat>Png</ImageFormat>
```

### ExportFileName <a href="#export_file_name" id="export_file_name"></a>

Полный путь до файла, в который будут выгружены данные.

Необязательный тэг. Любое значение будет переведено в текстовое.

Если тэг `<ExportFileName>` отсутствует, то имя файла выбирается произвольно в системной папке Temp.

Поддерживаются [константы замены](../values/replacement_constants.md).

```xml
<ExportFileName Ask="False">ExportFileName</ExportFileName>
```

#### Атрибуты тэга `<ExportFileName>` <a href="#attributes_tag_export_file_name" id="attributes_tag_export_file_name"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="465.3333333333333"></th></tr></thead><tbody><tr><td align="center">Ask</td><td><p>Признак, определяющий, будет ли задан вопрос о пути экспорта файла. </p><p></p><p>Необязательный атрибут. Ожидается логическое значение.</p><p></p><p>Если атрибут <code>Ask</code> отсутствует, то используется значение False.</p></td></tr></tbody></table>
