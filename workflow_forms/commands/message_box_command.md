---
description: Команда; открывает диалоговое окно сообщения.
---

# MessageBoxCommand

## Шаблон MessageBoxCommand <a href="#template_message_box_command" id="template_message_box_command"></a>

```xml
<Command Name="" Type="MessageBoxCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для MessageBoxCommand-->
  <Caption></Caption>
  <Text></Text>
  <Custom Value="" />
  <BackColor></BackColor>
  <ForeColor></ForeColor>
  <FontStyle></FontStyle>
  <MessageBoxStyle></MessageBoxStyle>
  <Link></Link>
  <LinkText></LinkText>
  <Icon Type="" />
  <Buttons Type="" />
  <CopyMode></CopyMode>
</Command>
```

## Описание MessageBoxCommand <a href="#description_message_box_command" id="description_message_box_command"></a>

```xml
<Command Name="MessageBoxCommandName" Type="MessageBoxCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для MessageBoxCommand-->
</Command>
```

### Результат выполнения <a href="#execution-result" id="execution-result"></a>

Результатом выполнения команды будет словарь, содержащий пары ключ-значение:

<table data-header-hidden><thead><tr><th align="center"></th><th width="437.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td>Значение нажатой кнопки - одно из <a href="message_box_command.md#values-of-parameter-value">списка</a></td></tr><tr><td align="center">OK</td><td>True, если была ли нажата кнопка OK</td></tr><tr><td align="center">Cancel</td><td>True, если была ли нажата кнопка Cancel ("Отмена")</td></tr><tr><td align="center">Abort</td><td>True, если была ли нажата кнопка Abort ("Прервать")</td></tr><tr><td align="center">Retry</td><td>True, если была ли нажата кнопка Retry ("Повторить")</td></tr><tr><td align="center">Ignore</td><td>True, если была ли нажата кнопка Ignore ("Пропустить")</td></tr><tr><td align="center">Yes</td><td>True, если была ли нажата кнопка Yes ("Да")</td></tr><tr><td align="center">No</td><td>True, если была ли нажата кнопка No ("Нет")</td></tr></tbody></table>

Так же в этом словаре будут ключи, соответствующие произвольным кнопкам, где в качестве ключа будет значение атрибута [`Result`](message_box_command.md#result).

Получить значение из словаря можно через атрибут `Parameter`, указав имя ключа:

```xml
<Command Name="MessageBoxCommandName" Parameter="Yes"/>
```

Для получения значения **Value** можно использовать сокращенную форму:

```xml
<Command Name="MessageBoxCommandName"/>
```

#### Значения параметра Value <a href="#values-of-parameter-value" id="values-of-parameter-value"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="437.3333333333333"></th></tr></thead><tbody><tr><td align="center">OK</td><td>Значение отправляется с кнопкой с надписью "OK"</td></tr><tr><td align="center">Cancel</td><td>Значение отправляется кнопкой с надписью "Отмена" ("Cancel")</td></tr><tr><td align="center">Abort</td><td>Значение отправляется кнопкой с надписью "Прервать" ("Abort")</td></tr><tr><td align="center">Retry</td><td>Значение отправляется кнопкой с надписью "Повторить" ("Retry")</td></tr><tr><td align="center">Ignore</td><td>Значение отправляется кнопкой "Пропустить" ("Ignore")</td></tr><tr><td align="center">Yes</td><td>Значение отправляется с кнопкой с надписью "Да" ("Yes")</td></tr><tr><td align="center">No</td><td>Значение отправляется с кнопкой с надписью "Нет" ("No")</td></tr></tbody></table>

Для произвольных кнопок параметр Value будет иметь значение, указанное в атрибуте [`Result`](message_box_command.md#result).

## Тэги, специфичные для MessageBoxCommand <a href="#tags_message_box_command" id="tags_message_box_command"></a>

### Caption <a href="#caption" id="caption"></a>

Заголовок диалогового окна.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Caption>Caption</Caption>
```

### Text <a href="#text" id="text"></a>

Текст внутри диалогового окна.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Text>Text</Text>
```

### Custom

Признак, отключающий возможность настраивать стиль диалогового окна.\
Если признак имеет значение False, то для внешнего вида диалогового окна используются настройки операционной системы.

Необязательный тэг. Значение тэга не ожидается.

Необязательный атрибут `Value` ожидает логическое значение. По умолчанию используется значение True.

```xml
<Custom Value="False" />
```

### BackColor <a href="#back_color" id="back_color"></a>

Цвет фона заголовка и тела диалогового окна.\
Игнорируется, если тэг [`<Custom>`](message_box_command.md#custom) имеет значение False.

Необязательный тэг. Ожидается имя одного из цветов, описанных в тэге [`<Appearance>`](../appearance.md) формы или в файле стилей. Так же принимается описание цвета в формате HTML (#rrggbb).&#x20;

По умолчанию используется белый цвет.

```xml
<BackColor>BackColor</BackColor>
```

### ForeColor <a href="#fore_color" id="fore_color"></a>

Цвет текста в теле и на кнопках диалогового окна.\
Игнорируется, если тэг [`<Custom>`](message_box_command.md#custom) имеет значение False.

Необязательный тэг. Ожидается имя одного из цветов, описанных в тэге [`<Appearance>`](../appearance.md) формы или в файле стилей. Так же принимается описание цвета в формате HTML (#rrggbb).&#x20;

По умолчанию используется черный цвет.

```xml
<ForeColor>ForeColor</ForeColor>
```

### FontStyle <a href="#font_style" id="font_style"></a>

Стиль шрифта в теле и на кастомных кнопках диалогового окна.\
Игнорируется, если тэг [`<Custom>`](message_box_command.md#custom) имеет значение False.

Необязательный тэг. Ожидается имя одного из стилей шрифтов, описанных в тэге [`<Appearance>`](../appearance.md) формы или в файле стилей.

По умолчанию используется значение `FontStyle`, которое указано для родительского объекта (если такового нет, то формы).

```xml
<FontStyle>FontStyle</FontStyle>
```

### MessageBoxStyle <a href="#message_box_style" id="message_box_style"></a>

Стиль для MessageBox.\
Игнорируется, если тэг [`<Custom>`](message_box_command.md#custom) имеет значение False.

Необязательный тэг. Ожидается имя одного из стилей, описанных в тэге [`<Appearance>`](../appearance.md) формы или в файле стилей.

```xml
<MessageBoxStyle>MessageBoxStyleName</MessageBoxStyle>
```

### Link

Определяет URL документа, на которую ведет ссылка. Результат перехода по ссылке зависит от конечного файла.\
Игнорируется, если тэг [`<Custom>`](message_box_command.md#custom) имеет значение False.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Link>URL</Link>
```

### LinkText

Задает видимый текст ссылки.\
Игнорируется, если тэг [`<Custom>`](message_box_command.md#custom) имеет значение False.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<LinkText>LinkText</LinkText>
```

### CopyMode <a href="#copy_mode" id="copy_mode"></a>

Задает режим копирования текста диалогового окна, указанного в тэге [`<Text>`](message_box_command.md#text).

Необязательный тэг. Ожидается название одного из режимов копирования:

<table data-header-hidden><thead><tr><th width="202.08667435984262" align="center"></th><th width="521.8817842146913"></th></tr></thead><tbody><tr><td align="center">Hotkey</td><td>Доступно копирование по Ctrl+C</td></tr><tr><td align="center">HotkeyButton</td><td>Доступно копирование по Ctrl+C и отображается кнопка копирования</td></tr><tr><td align="center">None</td><td>Возможность копирования отключена</td></tr></tbody></table>

По умолчанию используется значение Hotkey.

```xml
<CopyMode>HotkeyButton</CopyMode>
```

### Icon <a href="#icon" id="icon"></a>

Иконка диалогового окна.

Необязательный тэг. Значение тэга не ожидается.

```xml
<Icon Type="None" />
```

Для обязательного атрибута `Type` ожидается одно из допустимых значений:

<table data-header-hidden><thead><tr><th align="center"></th><th width="437.3333333333333"></th></tr></thead><tbody><tr><td align="center">None</td><td>Окно сообщения не содержит символов</td></tr><tr><td align="center">Hand</td><td>Окно сообщения содержит символ, состоящий из белого значка Х, заключенного в красный кружок</td></tr><tr><td align="center">Question</td><td>Окно сообщения содержит символ, состоящий из вопросительного знака, заключенного в кружок</td></tr><tr><td align="center">Exclamation</td><td>Окно сообщения содержит символ, состоящий из восклицательного знака в желтом треугольнике</td></tr><tr><td align="center">Asterisk</td><td>Окно сообщения содержит символ, состоящий из буквы i в нижнем регистре, помещенной в кружок</td></tr><tr><td align="center">Stop</td><td>Окно сообщения содержит символ, состоящий из белого значка Х, заключенного в красный кружок</td></tr><tr><td align="center">Error</td><td>Окно сообщения содержит символ, состоящий из белого значка Х, заключенного в красный кружок</td></tr><tr><td align="center">Warning</td><td>Окно сообщения содержит символ, состоящий из восклицательного знака в желтом треугольнике</td></tr><tr><td align="center">Information</td><td>Окно сообщения содержит символ, состоящий из буквы i в нижнем регистре, помещенной в кружок</td></tr></tbody></table>

По умолчанию для атрибута `Type` используется значение Information.

### Buttons <a href="#buttons" id="buttons"></a>

Набор кнопок диалогового окна. Можно выбрать предустановленный набор кнопок, используя атрибут `Type`, или описать произвольный набор кнопок, используя вложенный тэг [`<Button>`](message_box_command.md#description_button).

Необязательный тэг.

Вариант предустановленного списка кнопок:

```xml
<Buttons Type="Ok" />
```

Для обязательного атрибута `Type` ожидается одно из допустимых значений:

<table data-header-hidden><thead><tr><th align="center"></th><th width="460.3333333333333"></th></tr></thead><tbody><tr><td align="center">OK</td><td>Окно сообщения содержит кнопку "ОК"</td></tr><tr><td align="center">OKCancel</td><td>Окно сообщения содержит кнопки "ОК" и "Отмена"</td></tr><tr><td align="center">AbortRetryIgnore</td><td>Окно сообщения содержит кнопки "Прервать", "Повторить" и "Пропустить"</td></tr><tr><td align="center">YesNoCancel</td><td>Окно сообщения содержит кнопки "Да", "Нет" и "Отмена"</td></tr><tr><td align="center">YesNo</td><td>Окно сообщения содержит кнопки "Да" и "Нет"</td></tr><tr><td align="center">RetryCancel</td><td>Окно сообщения содержит кнопки "Повторить" и "Отмена"</td></tr></tbody></table>

По умолчанию для атрибута `Type` используется значение OK.

Вариант произвольного набора кнопок:

```xml
<Buttons>
  <Button Result="">
    <Width></Width>
    <Height></Height>
    <BackColor></BackColor>
    <Align></Align>
    <Index></Index>
    <FlatStyle></FlatStyle>
    <FlatBorderSize></FlatBorderSize>
    <FlatBorderColor></FlatBorderColor>
    <FlatMouseDownBackColor></FlatMouseDownBackColor>
    <FlatMouseOverBackColor></FlatMouseOverBackColor>
    <ForeColor></ForeColor>
    <FontStyle></FontStyle>
    <Image></Image>
    <ImageAlign></ImageAlign>
    <Text></Text>
    <TextAlign></TextAlign>
  </Button>
</Buttons>
```

***

## Описание Button <a href="#description_button" id="description_button"></a>

```xml
<Button Result="">
  <Width></Width>
  <Height></Height>
  <BackColor></BackColor>
  <Align></Align>
  <Index></Index>
  <FlatStyle></FlatStyle>
  <FlatBorderSize></FlatBorderSize>
  <FlatBorderColor></FlatBorderColor>
  <FlatMouseDownBackColor></FlatMouseDownBackColor>
  <FlatMouseOverBackColor></FlatMouseOverBackColor>
  <ForeColor></ForeColor>
  <FontStyle></FontStyle>
  <Image></Image>
  <ImageAlign></ImageAlign>
  <Text></Text>
  <TextAlign></TextAlign>
</Button>
```

### Атрибуты Button <a href="#attributes_button" id="attributes_button"></a>

#### Result

Значение, которое будет записываться в результат выполнения команды.

Обязательный атрибут. Любое значение будет переведено в текст.

### Height <a href="#button_height" id="button_height"></a>

Высота кнопки.

Необязательный тэг. Ожидается целочисленное значение.

По умолчанию используется значение 23.

```xml
<Height>25</Height>
```

### Width <a href="#button_width" id="button_width"></a>

Ширина кнопки.

Необязательный тэг. Ожидается целочисленное значение.

По умолчанию используется значение 90.

```xml
<Width>100</Width>
```

### BackColor <a href="#button_back_color" id="button_back_color"></a>

Цвет фона кнопки.

Необязательный тэг. Ожидается имя одного из цветов, описанных в тэге [`<Appearance>`](../appearance.md) формы или в файле стилей. Так же принимается описание цвета в формате HTML (#rrggbb).&#x20;

По умолчанию используется белый цвет.

```xml
<BackColor>BackColor</BackColor>
```

### FlatStyle <a href="#button_flat_style" id="button_flat_style"></a>

Задает тип границ кнопки.

Необязательный тэг. Ожидается название одного из стилей отображения кнопки:

<table data-header-hidden><thead><tr><th width="202.08667435984262" align="center"></th><th width="521.8817842146913"></th></tr></thead><tbody><tr><td align="center">Flat</td><td>Плоская</td></tr><tr><td align="center">Popup</td><td>Плоская, пока не наведена мышь</td></tr><tr><td align="center">Standard</td><td>Обычная</td></tr><tr><td align="center">System</td><td>Определяется операционной системой</td></tr></tbody></table>

По умолчанию используется значение Standard.

```xml
<FlatStyle>Standard</FlatStyle>
```

### FlatBorderSize <a href="#button_flat_border_size" id="button_flat_border_size"></a>

Задает размер границы плоской кнопки (кнопки, свойство [`<FlatStyle>`](message_box_command.md#button_flat_style) которой равно Flat).

Необязательный тэг. Ожидается целочисленное значение.

По умолчанию используется значение 1.

```xml
<FlatBorderSize>1</FlatBorderSize>
```

### FlatBorderColor <a href="#button_flat_border_color" id="button_flat_border_color"></a>

Задает цвет границы плоской кнопки (кнопки, свойство [`<FlatStyle>`](message_box_command.md#button_flat_style) которой равно Flat).

Необязательный тэг. Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется стандартное значение .NET.

```xml
<FlatBorderColor>FlatBorderColor</FlatBorderColor>
```

### FlatMouseDownBackColor <a href="#button_flat_mouse_down_back_color" id="button_flat_mouse_down_back_color"></a>

Задает цвет нажатой плоской кнопки (кнопки, свойство [`<FlatStyle>`](message_box_command.md#button_flat_style) которой равно Flat).

Необязательный тэг. Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

Если тэг `<FlatMouseDownBackColor>` отсутствует, то цвет рассчитывается автоматически.

```xml
<FlatMouseDownBackColor>FlatMouseDownBackColor</FlatMouseDownBackColor>
```

### FlatMouseOverBackColor <a href="#button_flat_mouse_over_back_color" id="button_flat_mouse_over_back_color"></a>

Задает цвет плоской кнопки при наведении курсора мыши (кнопки, свойство [`<FlatStyle>`](message_box_command.md#button_flat_style) которой равно Flat).

Необязательный тэг. Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

Если тэг `<FlatMouseOverBackColor>` отсутствует, то цвет рассчитывается автоматически.

```xml
<FlatMouseOverBackColor>FlatMouseOverBackColor</FlatMouseOverBackColor>
```

### Image <a href="#button_image" id="button_image"></a>

Путь до файла с графическим содержанием, которое будет расположено на кнопке.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Image>Image</Image>
```

### ImageAlign <a href="#button_image_align" id="button_image_align"></a>

Определяет тип положения картинки.

Необязательный тэг. Ожидается название одного из типов положения картинки:

<table data-header-hidden><thead><tr><th align="center"></th><th width="464.2197125256674"></th></tr></thead><tbody><tr><td align="center">TopLeft</td><td>Слева сверху</td></tr><tr><td align="center">TopCenter</td><td>По центру сверху</td></tr><tr><td align="center">TopRight</td><td>Справа сверху</td></tr><tr><td align="center">MiddleLeft</td><td>Слева посередине</td></tr><tr><td align="center">MiddleCenter</td><td>По центру посередине</td></tr><tr><td align="center">MiddleRight</td><td>Справа посередине</td></tr><tr><td align="center">BottomLeft</td><td>Слева снизу</td></tr><tr><td align="center">BottomCenter</td><td>По центру снизу</td></tr><tr><td align="center">BottomRight</td><td>Справа снизу</td></tr></tbody></table>

По умолчанию используется значение MiddleCente&#x72;**.**

```xml
<ImageAlign>MiddleCenter</ImageAlign>
```

### ForeColor <a href="#button_fore_color" id="button_fore_color"></a>

Цвет текста на кнопке.

Необязательный тэг. Ожидается имя одного из цветов, описанных в тэге [`<Appearance>`](../appearance.md) формы или в файле стилей. Так же принимается описание цвета в формате HTML (#rrggbb).&#x20;

По умолчанию используется значение `ForeColor`, которое указано для диалогового окна.

```xml
<ForeColor>ForeColor</ForeColor>
```

### FontStyle <a href="#button_font_style" id="button_font_style"></a>

Стиль шрифта текста на кнопке.

Необязательный тэг. Ожидается имя одного из стилей шрифтов, описанных в тэге [`<Appearance>`](../appearance.md) формы или в файле стилей.

По умолчанию используется значение `FontStyle`, которое указано для диалогового окна.

```xml
<FontStyle>FontStyle</FontStyle>
```

### Text <a href="#button_text" id="button_text"></a>

Текст на кнопке.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Text>Текст</Text>
```

### TextAlign <a href="#button_text_align" id="button_text_align"></a>

Определяет тип положения текста.

Необязательный тэг. Ожидается название одного из типов положения текста:

<table data-header-hidden><thead><tr><th align="center"></th><th width="438.3333333333333"></th></tr></thead><tbody><tr><td align="center">TopLeft</td><td>Слева сверху</td></tr><tr><td align="center">TopCenter</td><td>По центру сверху</td></tr><tr><td align="center">TopRight</td><td>Справа сверху</td></tr><tr><td align="center">MiddleLeft</td><td>Слева посередине</td></tr><tr><td align="center">MiddleCenter</td><td>По центру посередине</td></tr><tr><td align="center">MiddleRight</td><td>Справа посередине</td></tr><tr><td align="center">BottomLeft</td><td>Слева снизу</td></tr><tr><td align="center">BottomCenter</td><td>По центру снизу</td></tr><tr><td align="center">BottomRight</td><td>Справа снизу</td></tr></tbody></table>

По умолчанию используется значение MiddleLeft.

```xml
<TextAlign>MiddleLeft</TextAlign>
```

### Align <a href="#button_align" id="button_align"></a>

Определяет тип положения кнопки.

Необязательный тэг. Ожидается название одного из типов положения кнопки:

<table data-header-hidden><thead><tr><th align="center"></th><th width="438.3333333333333"></th></tr></thead><tbody><tr><td align="center">Left</td><td>Слева снизу</td></tr><tr><td align="center">Center</td><td>По центру снизу</td></tr><tr><td align="center">Right</td><td>Справа снизу</td></tr></tbody></table>

По умолчанию используется значение Right.

```xml
<Align>Left</Align>
```

### Index <a href="#button_index" id="button_index"></a>

Задает порядок отображения кнопки в диалоговом окне.\
Если несколько кнопок имеет одинаковое значение тэга, или тэг отсутствует, то кнопки отображаются в порядке описания в xml-коде.

Необязательный тэг. Ожидается целочисленное значение.

По умолчанию используется значение 0.

```xml
<Index>3</Index>
```
