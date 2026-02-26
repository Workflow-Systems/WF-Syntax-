---
description: Команда; открывает диалоговое окно выбора папки.
---

# FolderDialogShowCommand

## Шаблон FolderDialogShowCommand <a href="#template_folder_dialog_show_command" id="template_folder_dialog_show_command"></a>

```xml
<Command Name="" Type="FolderDialogShowCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для FolderDialogShowCommand-->
  <Title></Title>
  <RootSpecialFolder></RootSpecialFolder>
  <SelectedPath></SelectedPath>
  <ShowNewFolderButton></ShowNewFolderButton>
</Command>
```

## Описание FolderDialogShowCommand <a href="#description_folder_dialog_show_command" id="description_folder_dialog_show_command"></a>

```xml
<Command Name="FolderDialogShowCommandName" Type="FolderDialogShowCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для FolderDialogShowCommand-->
</Command>
```

### Результат выполнения FolderDialogShowCommand <a href="#result_folder_dialog_show_command" id="result_folder_dialog_show_command"></a>

#### OK <a href="#result_ok" id="result_ok"></a>

Признак того, что в диалоговом окне пользователем была выбрана папка.

#### Path <a href="#result_path" id="result_path"></a>

Полный путь до выбранной папки.

#### FolderName <a href="#result_folder_name" id="result_folder_name"></a>

Имя выбранной папки.

## Тэги, специфичные для FolderDialogShowCommand <a href="#tags_folder_dialog_show_command" id="tags_folder_dialog_show_command"></a>

### Title <a href="#title" id="title"></a>

Заголовок диалогового окна.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Title>Title</Title>
```

### RootSpecialFolder <a href="#root_special_folder" id="root_special_folder"></a>

Название одной из [специальных корневых директорий](folder_dialog_show_command.md#special_folder_types) диалогового окна.

Необязательный тэг. Любое значение будет переведено в текстовое.

Если тэг `<RootSpecialFolder>` отсутствует, то используется стандартное значение .NET.

#### Специальные корневые директории диалогового окна <a href="#special_folder_types" id="special_folder_types"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="474.3333333333333"></th></tr></thead><tbody><tr><td align="center">Desktop</td><td>Рабочий стол</td></tr><tr><td align="center">MyComputer</td><td>Мой компьютер</td></tr><tr><td align="center">MyDocuments</td><td>Папка "Мои документы"</td></tr><tr><td align="center">Network</td><td>Сетевое окружение / сеть</td></tr></tbody></table>

Все поддерживаемые названия специальных корневых директорий смотрите по [ссылке](http://msdn.microsoft.com/ru-ru/library/system.environment.specialfolder\(v=vs.110\).aspx).

```xml
<RootSpecialFolder>Desktop</RootSpecialFolder>
```

### SelectedPath <a href="#selected_path" id="selected_path"></a>

Путь до выбранной папки, задаваемый по умолчанию.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<SelectedPath>SelectedPath</SelectedPath>
```

### ShowNewFolderButton <a href="#show_new_folder_button" id="show_new_folder_button"></a>

Признак, определяющий, будет ли кнопка "Новая папка" в диалоговом окне.

Необязательный тэг. Ожидается логическое значение.

Если тэг `<ShowNewFolderButton>` отсутствует, то используется значение True.

```xml
<ShowNewFolderButton>True</ShowNewFolderButton>
```
