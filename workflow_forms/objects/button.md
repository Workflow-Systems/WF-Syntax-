---
description: >-
  Графический объект; кнопка, по нажатию на которую выполняются определенные
  команды.
---

# Button

## Шаблон Button <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="" Type="Button" Assembly="BaseControls" ChangeForm="">
  <!--Тэги, общие для всех графических объектов-->
  <Top></Top>
  <Bottom></Bottom>
  <Left></Left>
  <Right></Right>
  <Height></Height>
  <Width></Width>
  <FontStyle></FontStyle>
  <ForeColor></ForeColor>
  <BackColor></BackColor>
  <Enabled></Enabled>
  <Visible></Visible>
  <Hint></Hint>
  <ContextMenu Name="" />
  <Change User="" Source="" ValueSet="" />
  <!--Тэги, специфичные для Button-->
  <Blink></Blink>
  <BlinkInterval></BlinkInterval>
  <BlinkPart></BlinkPart>
  <FlatStyle></FlatStyle>
  <FlatBorderSize></FlatBorderSize>
  <FlatBorderColor></FlatBorderColor>
  <FlatMouseDownBackColor></FlatMouseDownBackColor>
  <FlatMouseOverBackColor></FlatMouseOverBackColor>
  <Image></Image>
  <ImageAlign></ImageAlign>
  <BackgroundImage></BackgroundImage>
  <BackgroundImageLayout></BackgroundImageLayout>
  <DisabledMode></DisabledMode>
  <DisabledText></DisabledText>
  <TextAlign></TextAlign>
  <Text></Text>
  <Commands StopOnError="" Lock="">
    <Command Name="" />
    <If>
      <When></When>
      <Then StopOnError="" Lock="">
        <Command Name="" />
      </Then>
      <ElseIf>
        <When></When>
        <Then StopOnError="" Lock="">
          <Command Name="">
            <Input Name="" />
            <Input Name="" />
          </Command>
        </Then>
      </ElseIf>
      <Else StopOnError="" Lock="">
        <Command Name="" />
      </Else>
    </If>
  </Commands>
</MyObject>
```

## Описание Button <a href="#description" id="description"></a>

```xml
<MyObject Name="ButtonName" Type="Button" Assembly="BaseControls">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для Button-->
</MyObject>
```

Значением Button считается текст, указанный на кнопке.

### Получение значения <a href="#get-value" id="get-value"></a>

Для получения указанного на кнопке текста используется get-проперти [Text](button.md#text-1):

```xml
<Object Name="ButtonName">
  <Property Name="Text" />
</Object>
```

Рекомендуется использовать сокращенный вариант записи:

```xml
<Object Name="ButtonName" />
```

### Задание значения <a href="#set-value" id="set-value"></a>

Для задания отображаемого на кнопке текста используется set-проперти [Text](button.md#set_text):

```xml
<Object Name="ButtonName">
  <Property Name="Text">Text</Property>
</Object>
```

Рекомендуется использовать сокращенный вариант записи:

```xml
<Object Name="ButtonName">Text</Object>
```

## Тэги, специфичные для Button <a href="#specific-tags" id="specific-tags"></a>

### Blink

Признак, включающий режим мигания.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<Blink>True</Blink>
```

### BlinkInterval <a href="#blink_interval" id="blink_interval"></a>

Задает интервал мигания (в миллисекундах).

Необязательный тэг. Ожидается целочисленное значение.

По умолчанию используется значение 500.

```xml
<BlinkInterval>500</BlinkInterval>
```

### BlinkPart <a href="#blink_part" id="blink_part"></a>

Признак, определяющий режим мигания: только текст, только изображение или текст и изображение одновременно.

Необязательный тэг. Ожидается название одного из режимов:

<table data-header-hidden><thead><tr><th width="202.08667435984262" align="center"></th><th width="521.8817842146913"></th></tr></thead><tbody><tr><td align="center">All</td><td>Мигают и текст и изображение</td></tr><tr><td align="center">Text</td><td>Мигает только текст</td></tr><tr><td align="center">Image</td><td>Мигает только изображение</td></tr></tbody></table>

По умолчанию используется значение All.

```xml
<BlinkPart>Image</BlinkPart>
```

### FlatStyle <a href="#flat_style" id="flat_style"></a>

Задает тип границ кнопки.

Необязательный тэг. Ожидается название одного из стилей отображения кнопки:

<table data-header-hidden><thead><tr><th width="202.08667435984262" align="center"></th><th width="521.8817842146913"></th></tr></thead><tbody><tr><td align="center">Flat</td><td>Плоская</td></tr><tr><td align="center">Popup</td><td>Плоская, пока не наведена мышь</td></tr><tr><td align="center">Standard</td><td>Обычная</td></tr><tr><td align="center">System</td><td>Определяется операционной системой</td></tr></tbody></table>

По умолчанию используется значение Standard.

```xml
<FlatStyle>Standard</FlatStyle>
```

### FlatBorderSize <a href="#flat_border_size" id="flat_border_size"></a>

Задает размер границы плоской кнопки (кнопки, свойство [`<FlatStyle>`](button.md#flat_style) которой равно Flat).

Необязательный тэг. Ожидается целочисленное значение.

По умолчанию используется значение 1.

```xml
<FlatBorderSize>1</FlatBorderSize>
```

### FlatBorderColor <a href="#flat_border_color" id="flat_border_color"></a>

Задает цвет границы плоской кнопки (кнопки, свойство [`<FlatStyle>`](button.md#flat_style) которой равно Flat).

Необязательный тэг. Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется стандартное значение .NET.

```xml
<FlatBorderColor>FlatBorderColor</FlatBorderColor>
```

### FlatMouseDownBackColor <a href="#flat_mouse_down_back_color" id="flat_mouse_down_back_color"></a>

Задает цвет нажатой плоской кнопки (кнопки, свойство [`<FlatStyle>`](button.md#flat_style) которой равно Flat).

Необязательный тэг. Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

Если тэг `<FlatMouseDownBackColor>` отсутствует, то цвет рассчитывается автоматически.

```xml
<FlatMouseDownBackColor>FlatMouseDownBackColor</FlatMouseDownBackColor>
```

### FlatMouseOverBackColor <a href="#flat_mouse_over_back_color" id="flat_mouse_over_back_color"></a>

Задает цвет плоской кнопки при наведении курсора мыши (кнопки, свойство [`<FlatStyle>`](button.md#flat_style) которой равно Flat).

Необязательный тэг. Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

Если тэг `<FlatMouseOverBackColor>` отсутствует, то цвет рассчитывается автоматически.

```xml
<FlatMouseOverBackColor>FlatMouseOverBackColor</FlatMouseOverBackColor>
```

### Image

Путь до файла с графическим содержанием, которое будет расположено на кнопке.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Image>Image</Image>
```

### ImageAlign <a href="#image_align" id="image_align"></a>

Определяет тип положения картинки.

Необязательный тэг. Ожидается название одного из типов положения картинки:

<table data-header-hidden><thead><tr><th align="center"></th><th width="464.2197125256674"></th></tr></thead><tbody><tr><td align="center">TopLeft</td><td>Слева сверху</td></tr><tr><td align="center">TopCenter</td><td>По центру сверху</td></tr><tr><td align="center">TopRight</td><td>Справа сверху</td></tr><tr><td align="center">MiddleLeft</td><td>Слева посередине</td></tr><tr><td align="center">MiddleCenter</td><td>По центру посередине</td></tr><tr><td align="center">MiddleRight</td><td>Справа посередине</td></tr><tr><td align="center">BottomLeft</td><td>Слева снизу</td></tr><tr><td align="center">BottomCenter</td><td>По центру снизу</td></tr><tr><td align="center">BottomRight</td><td>Справа снизу</td></tr></tbody></table>

По умолчанию используется значение MiddleCente&#x72;**.**

```xml
<ImageAlign>MiddleCenter</ImageAlign>
```

### BackgroundImage <a href="#background_image" id="background_image"></a>

Путь до файла с графическим содержанием, которое будет расположено на кнопке.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<BackgroundImage>BackgroundImage</BackgroundImage>
```

### BackgroundImageLayout <a href="#background_image_layout" id="background_image_layout"></a>

Определяет тип расположения графического содержания на кнопке.

Необязательный тэг. Ожидается название одного из типов расположения графического содержания на кнопке:

<table data-header-hidden><thead><tr><th width="150" align="center"></th><th width="442.3333333333333"></th></tr></thead><tbody><tr><td align="center">None</td><td>Изображение выравнивается на кнопке вверху по левой стороне</td></tr><tr><td align="center">Tile</td><td>Выполняется мозаичное заполнение изображением кнопки</td></tr><tr><td align="center">Center</td><td>Изображение центрируется на кнопке</td></tr><tr><td align="center">Stretch</td><td>Изображение растягивается на всю длину кнопки</td></tr><tr><td align="center">Zoom</td><td>Изображение увеличивается в пределах кнопки</td></tr></tbody></table>

По умолчанию используется значение Tile.

```xml
<BackgroundImageLayout>Tile</BackgroundImageLayout>
```

### TextAlign <a href="#text_align" id="text_align"></a>

Определяет тип положения текста.

Необязательный тэг. Ожидается название одного из типов положения текста:

<table data-header-hidden><thead><tr><th align="center"></th><th width="438.3333333333333"></th></tr></thead><tbody><tr><td align="center">TopLeft</td><td>Слева сверху</td></tr><tr><td align="center">TopCenter</td><td>По центру сверху</td></tr><tr><td align="center">TopRight</td><td>Справа сверху</td></tr><tr><td align="center">MiddleLeft</td><td>Слева посередине</td></tr><tr><td align="center">MiddleCenter</td><td>По центру посередине</td></tr><tr><td align="center">MiddleRight</td><td>Справа посередине</td></tr><tr><td align="center">BottomLeft</td><td>Слева снизу</td></tr><tr><td align="center">BottomCenter</td><td>По центру снизу</td></tr><tr><td align="center">BottomRight</td><td>Справа снизу</td></tr></tbody></table>

По умолчанию используется значение MiddleLeft.

```xml
<TextAlign>MiddleLeft</TextAlign>
```

### Text

Текст на кнопке.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Text>Текст</Text>
```

### DisabledMode <a href="#disabled_mode" id="disabled_mode"></a>

Признак, при установке которого при нажатии на неактивную кнопку (Enabled = False) будет показано сообщение с текстом, указанным в тэге [`<DisabledText>`](button.md#disabled_text).

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<DisabledMode>False</DisabledMode>
```

### DisabledText <a href="#disabled_text" id="disabled_text"></a>

Текст сообщения, которое будет показано по нажатию на неактивную кнопку с установленным признаком [`<DisabledMode>`](button.md#disabledmode).

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<DisabledText>Текст сообщения</DisabledText>
```

### Commands

Список команд, которые будут выполнены при нажатии на кнопку.

Необязательный тэг. В качестве значения тэга ожидается список тэгов [`<Command>`](button.md#teg-less-than-command-greater-than) и/или конструкций [`<If>`](../values/if.md).

```xml
<Commands StopOnError="True"  Lock="">
  <Command Name="CommandName1" />
  <If>
    <When></When>
    <Then StopOnError="True" Lock="">
      <Command Name="CommandName2">
        <Input Name="InputName1">input 1</Input>
        <Input Name="InputName2">input 2</Input>
      </Command>
    </Then>
    <ElseIf>
      <When></When>
      <Then StopOnError="True" Lock="">
        <Command Name="CommandName3" />
      </Then>
    </ElseIf>
    <Else StopOnError="True" Lock="">
      <Command Name="CommandName4" />
    </Else>
  </If>
</Commands>
```

#### Атрибуты тэга `<Commands>`

<table data-header-hidden><thead><tr><th width="150" align="center"></th><th width="532.4285714285713"></th></tr></thead><tbody><tr><td align="center">StopOnError</td><td><p>Признак, определяющий, будет ли остановлено выполнение команд, если при выполнении очередной произойдет ошибка.</p><p></p><p>Необязательный атрибут. Ожидается логическое значение.</p><p></p><p>По умолчанию используется значение True.</p></td></tr><tr><td align="center">Lock</td><td><p>Признак, определяющий, будет ли блокироваться форма при выполнении команд.</p><p></p><p>Необязательный атрибут. Ожидается логическое значение.</p><p></p><p>По умолчанию используется значение False.</p></td></tr></tbody></table>

#### Тэг `<Command>`

Обращение к команде по имени для ее выполнения.

Необязательный тэг. В качестве значения тэга ожидается список тэгов [`<Input>`](../values/input.md).

```xml
<!--Вариант 1-->
<Command Name="CommandName1" />

<!--Вариант 2-->
<Command Name="CommandName2">
  <Input Name="InputName1">input 1</Input>
  <Input Name="InputName2">input 2</Input>
</Command>
```

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### Blink <a href="#get_blink" id="get_blink"></a>

Возвращает значение признака мигания.

```xml
<Object Name="LabelName">
  <Property Name="Blink" />
</Object>
```

### BlinkInterval <a href="#get_blink_interval" id="get_blink_interval"></a>

Возвращает интервал мигания (в миллисекундах).

```xml
<Object Name="LabelName">
  <Property Name="BlinkInterval" />
</Object>
```

### BlinkPart <a href="#get_blink_part" id="get_blink_part"></a>

Возвращает название режима мигания.

```xml
<Object Name="ButtonName">
  <Property Name="BlinkPart" />
</Object>
```

### FlatStyle <a href="#get_flat_style" id="get_flat_style"></a>

Возвращает название типа границ кнопки.

```xml
<Object Name="ButtonName">
  <Property Name="FlatStyle" />
</Object>
```

### FlatBorderSize <a href="#get_flat_border_size" id="get_flat_border_size"></a>

Возвращает размер границы плоской кнопки (кнопки, свойство [`<FlatStyle>`](button.md#flat_style) которой равно Flat).

```xml
<Object Name="ButtonName">
  <Property Name="FlatBorderSize" />
</Object>
```

### FlatBorderColor <a href="#get_flat_border_color" id="get_flat_border_color"></a>

Возвращает имя цвета границы плоской кнопки (кнопки, свойство [`<FlatStyle>`](button.md#flat_style) которой равно Flat).

```xml
<Object Name="ButtonName">
  <Property Name="FlatBorderColor" />
</Object>
```

### FlatMouseDownBackColor <a href="#get_flat_mouse_down_back_color" id="get_flat_mouse_down_back_color"></a>

Возвращает имя цвета нажатой плоской кнопки (кнопки, свойство [`<FlatStyle>`](button.md#flat_style) которой равно Flat).

```xml
<Object Name="ButtonName">
  <Property Name="FlatMouseDownBackColor" />
</Object>
```

### FlatMouseOverBackColor <a href="#get_flat_mouse_over_back_color" id="get_flat_mouse_over_back_color"></a>

Возвращает имя цвета плоской кнопки при наведении курсора мыши (кнопки, свойство [`<FlatStyle>`](button.md#flat_style) которой равно Flat).

```xml
<Object Name="ButtonName">
  <Property Name="FlatMouseOverBackColor" />
</Object>
```

### Image <a href="#get_image" id="get_image"></a>

Возвращает путь до файла с графическим содержанием, которое будет расположено на кнопке.

```xml
<Object Name="ButtonName">
  <Property Name="Image" />
</Object>
```

### ImageAlign <a href="#get_image_align" id="get_image_align"></a>

Возвращает название типа положения картинки.

```xml
<Object Name="ButtonName">
  <Property Name="ImageAlign" />
</Object>
```

### BackgroundImage <a href="#get_background_image" id="get_background_image"></a>

Возвращает путь до файла с графическим содержанием, которое будет расположено на кнопке.

```xml
<Object Name="ButtonName">
  <Property Name="BackgroundImage" />
</Object>
```

### BackgroundImageLayout <a href="#get_background_image_layout" id="get_background_image_layout"></a>

Возвращает название типа расположения графического содержания на кнопке.

```xml
<Object Name="ButtonName">
  <Property Name="BackgroundImageLayout" />
</Object>
```

### TextAlign <a href="#get_text_align" id="get_text_align"></a>

Возвращает название типа положения текста.

```xml
<Object Name="ButtonName">
  <Property Name="TextAlign" />
</Object>
```

### Text

Возвращает текст на кнопке.

```xml
<Object Name="ButtonName">
  <Property Name="Text" />
</Object>
```

### DisabledMode <a href="#get_disabled_mode" id="get_disabled_mode"></a>

Возвращает значение признака [`<DisabledMode>`](button.md#disabled_mode).

```xml
<Object Name="ButtonName">
  <Property Name="DisabledMode" />
</Object>
```

### DisabledText <a href="#get_disabled_text" id="get_disabled_text"></a>

Возвращает текст сообщения, заданное для признака [`<DisabledText>`](button.md#disabled_text).

```xml
<Object Name="ButtonName">
  <Property Name="DisabledText" />
</Object>
```

## Set-проперти для динамического задания свойств <a href="#get-properties" id="get-properties"></a>

### Blink <a href="#set_blink" id="set_blink"></a>

Задает признак мигания.

Ожидается логическое значение.

```xml
<Object Name="LabelName">
  <Property Name="Blink">True</Property>
</Object>
```

### BlinkInterval <a href="#set_blink_interval" id="set_blink_interval"></a>

Задает интервал мигания (в миллисекундах).

Ожидается целочисленное значение.

```xml
<Object Name="LabelName">
  <Property Name="BlinkInterval">1000</Property>
</Object>
```

### BlinkPart <a href="#set_blink_part" id="set_blink_part"></a>

Задает название режима мигания.

Ожидается одно из названий режимов мигания.

```xml
<Object Name="ButtonName">
  <Property Name="BlinkPart">Text</Property>
</Object>
```

### FlatStyle <a href="#set_flat_style" id="set_flat_style"></a>

Задает название типа границ кнопки.

Ожидается одно из названий типов границ кнопки.

```xml
<Object Name="ButtonName">
  <Property Name="FlatStyle">Popup</Property>
</Object>
```

### FlatBorderSize <a href="#set_flat_border_size" id="set_flat_border_size"></a>

Задает размер границы плоской кнопки (кнопки, свойство [`<FlatStyle>`](button.md#flat_style) которой равно Flat).

Ожидается целочисленное значение.

```xml
<Object Name="ButtonName">
  <Property Name="FlatBorderSize">1</Property>
</Object>
```

### FlatBorderColor <a href="#set_flat_border_color" id="set_flat_border_color"></a>

Задает имя цвета границы плоской кнопки (кнопки, свойство [`<FlatStyle>`](button.md#flat_style) которой равно Flat).

Ожидается название одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

```xml
<Object Name="ButtonName">
  <Property Name="FlatBorderColor">FlatBorderColor</Property>
</Object>
```

### FlatMouseDownBackColor <a href="#set_flat_mouse_down_back_color" id="set_flat_mouse_down_back_color"></a>

Задает имя цвета нажатой плоской кнопки (кнопки, свойство [`<FlatStyle>`](button.md#flat_style) которой равно Flat).

Ожидается название одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

```xml
<Object Name="ButtonName">
  <Property Name="FlatMouseDownBackColor">FlatMouseDownBackColor</Property>
</Object>
```

### FlatMouseOverBackColor <a href="#set_flat_mouse_over_back_color" id="set_flat_mouse_over_back_color"></a>

Задает имя цвета плоской кнопки при наведении курсора мыши (кнопки, свойство [`<FlatStyle>`](button.md#flat_style) которой равно Flat).

Ожидается название одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

```xml
<Object Name="ButtonName">
  <Property Name="FlatMouseOverBackColor">FlatMouseOverBackColor</Property>
</Object>
```

### Image <a href="#set_image" id="set_image"></a>

Задает путь до файла с графическим содержанием, которое будет расположено на кнопке.

Любое значение будет переведено в текстовое.

```xml
<Object Name="ButtonName">
  <Property Name="Image" />
</Object>
```

### ImageAlign <a href="#set_image_align" id="set_image_align"></a>

Задает название типа положения картинки.

Ожидается одно из названий типов положения картинки.

```xml
<Object Name="ButtonName">
    <Property Name="ImageAlign">TopLeft</Property>
</Object>
```

### BackgroundImage <a href="#set_background_image" id="set_background_image"></a>

Задает путь до файла с графическим содержанием, которое будет расположено на кнопке.

Любое значение будет переведено в текстовое.

```xml
<Object Name="ButtonName">
  <Property Name="BackgroundImage" />
</Object>
```

### BackgroundImageLayout <a href="#set_background_image_layout" id="set_background_image_layout"></a>

Задает название типа расположения графического содержания на кнопке.

Ожидается одно из названий типов расположения графического содержания на кнопке.

```xml
<Object Name="ButtonName">
  <Property Name="BackgroundImageLayout" />
</Object>
```

### TextAlign <a href="#set_text_align" id="set_text_align"></a>

Задает название типа положения текста.

Ожидается одно из названий типов положения текста.

```xml
<Object Name="ButtonName">
  <Property Name="TextAlign">TopLeft</Property>
</Object>
```

### Text

Задает текст на кнопке.

Любое значение будет переведено в текстовое.

```xml
<Object Name="ButtonName">
  <Property Name="Text">Text</Property>
</Object>
```

### DisabledMode <a href="#get_disabled_mode" id="get_disabled_mode"></a>

Задает значение признака [`<DisabledMode>`](button.md#disabled_mode).

```xml
<Object Name="ButtonName">
  <Property Name="DisabledMode" />
</Object>
```

### DisabledText <a href="#get_disabled_text" id="get_disabled_text"></a>

Задает текст сообщения для признака [`<DisabledText>`](button.md#disabled_text).

```xml
<Object Name="ButtonName">
  <Property Name="DisabledText" />
</Object>
```
