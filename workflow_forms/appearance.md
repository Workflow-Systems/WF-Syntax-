---
description: Описание графических настроек отображения формы.
---

# Appearance

## Описание Appearance <a href="#description_appearance" id="description_appearance"></a>

```xml
<Appearance>
  <Colors>
    <Color Name="" Red="" Green="" Blue="" Alpha="" />
  </Colors>
  
  <FontStyles>
    <FontStyle Name="" Font="" FromFile="" Size="" Bold="" Italic="" Underline="" Strikeout="" />
  </FontStyles>
  
  <Styles>
    <MessageBoxStyle Name="" Default="">
      <DelimeterStartForeColor></DelimeterStartForeColor>
    </MessageBoxStyle>
  </Styles>
</Appearance>
```

#### Colors <a href="#colors" id="colors"></a>

Необязательный тэг. Содержит список необязательных тэгов [`<Color>`](appearance.md#color), описывающих цвета.

#### FontStyles <a href="#font_styles" id="font_styles"></a>

Необязательный тэг. Содержит список необязательных тэгов [`<FontStyle>`](appearance.md#font_style), описывающих стили шрифтов.

#### Styles

Необязательный тэг. Содержит список необязательных тэгов [`<MessageBoxStyle>`](appearance.md#message_box_style), описывающих стили диалоговых окон.

## Color <a href="#color" id="color"></a>

Цвет.

```xml
<Color Name="" Red="" Green="" Blue="" Alpha="" />
```

### Атрибуты Color <a href="#attributes_color" id="attributes_color"></a>

#### Name <a href="#color_name" id="color_name"></a>

Название цвета.\
Обязательный атрибут. Значение атрибута любое значение.

#### Red <a href="#color_red" id="color_red"></a>

Красная составляющая цвета.\
Обязательный атрибут. Ожидается целочисленное значение (от 0 до 255).

#### Green <a href="#color_green" id="color_green"></a>

Зеленая составляющая цвета.\
Обязательный атрибут. Ожидается целочисленное значение (от 0 до 255).

#### Blue <a href="#color_blue" id="color_blue"></a>

Синяя составляющая цвета.\
Обязательный атрибут. Ожидается целочисленное значение (от 0 до 255).

#### Alpha <a href="#color_alpha" id="color_alpha"></a>

Составляющая насыщенности цвета.\
Обязательный атрибут. Ожидается целочисленное значение (от 0 до 255).

## FontStyle <a href="#font_style" id="font_style"></a>

Стиль шрифта.

Необязательный тэг. Значение тэга не ожидается.

```xml
<FontStyle Name=""
           Font=""
           FromFile=""
           Size=""
           Bold=""
           Italic=""
           Underline=""
           Strikeout="" />
```

### Атрибуты FontStyle <a href="#attributes_font_style" id="attributes_font_style"></a>

#### Name <a href="#font_style_name" id="font_style_name"></a>

Название стиля шрифта.\
Обязательный атрибут. Значение атрибута любое значение.

#### Font <a href="#font_style_font" id="font_style_font"></a>

Название системного шрифта.\
Необязательный атрибут. Значение атрибута название одного из системных шрифтов.

Если атрибут `Font` отсутствует, то шрифт загружается из файла по пути, указанном в атрибуте `FromFile`.

#### FromFile <a href="#font_style_from_file" id="font_style_from_file"></a>

Путь до файла со шрифтом.\
Необязательный атрибут. Значение атрибута `FromFile`: любое значение.

Если атрибут `FromFile` отсутствует, то шрифт загружается из системы по имени, указанному в атрибуте `Font`.

#### Size <a href="#font_style_size" id="font_style_size"></a>

Размер шрифта.\
Обязательный атрибут. Ожидается целочисленное значение (от 1).

#### Bold <a href="#font_style_bold" id="font_style_bold"></a>

Признак оформления шрифта жирным.\
Необязательный атрибут. Ожидается логическое значение.

По умолчанию используется значение False.

#### Italic <a href="#font_style_italic" id="font_style_italic"></a>

Признак оформления шрифта курсивом.\
Необязательный атрибут. Ожидается логическое значение.

По умолчанию используется значение False.

#### Underline <a href="#font_style_underline" id="font_style_underline"></a>

Признак оформления шрифта подчеркиванием.\
Необязательный атрибут. Ожидается логическое значение.

По умолчанию используется значение False.

#### Strikeout <a href="#font_style_strikeout" id="font_style_strikeout"></a>

Признак оформления шрифта зачеркиванием.\
Необязательный атрибут. Ожидается логическое значение.

По умолчанию используется значение False.

## MessageBoxStyle <a href="#message_box_style" id="message_box_style"></a>

Стиль диалогового окна.

```xml
<MessageBoxStyle Name="" Default="">
  <DelimeterStartForeColor></DelimeterStartForeColor>
</MessageBoxStyle>
```

### Атрибуты MessageBoxStyle <a href="#attributes_message_box_style" id="attributes_message_box_style"></a>

#### Name <a href="#message_box_style_name" id="message_box_style_name"></a>

Название стиля диалогового окна.\
Обязательный атрибут. Значение атрибута любое значение.

#### Default <a href="#message_box_style_default" id="message_box_style_default"></a>

Признак, определяющий стиль по умолчанию для всех MessageBoxCommand.\
Необязательный атрибут. Ожидается логическое значение.

По умолчанию используется значение False.

{% hint style="warning" %}
Стилем по умолчанию может быть только один MessageBoxStyle. Если нет ни одного MessageBoxStyle с атрибутом Default со значениемTrue, то стилем по умолчанию считается первый в порядке описания стиль.
{% endhint %}

### DelimeterStartForeColor <a href="#msg_delimeter_start_fore_color" id="msg_delimeter_start_fore_color"></a>

Начальный цвет разделителя.

Необязательный тэг. Ожидается имя одного из цветов, описанных в тэге [`<Appearance>`](appearance.md) формы или в файле стилей. Так же принимается описание цвета в формате HTML (#rrggbb).&#x20;
