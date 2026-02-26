---
description: >-
  Индикатор, отображающий выполнение определенного процесса. Элемент
  пользовательского интерфейса.
---

# ProgressBar

## Шаблон ProgressBar <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="ProgressBarName" Type="ProgressBar" Assembly="BaseControls">
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
  <!--Тэги, специфичные для ProgressBar-->
  <Custom Value="" />
  <Minimum></Minimum>
  <Maximum></Maximum>
  <Value></Value>
  <BorderColor></BorderColor>
  <BorderWidth></BorderWidth>
  <ChannelHeight></ChannelHeight>
  <ChannelGradient></ChannelGradient>
  <ChannelFirstColor></ChannelFirstColor>
  <ChannelSecondColor></ChannelSecondColor>
  <SliderHeight></SliderHeight>
  <SliderGradient></SliderGradient>
  <SliderFirstColor></SliderFirstColor>
  <SliderSecondColor></SliderSecondColor>
  <TextAlign></TextAlign>
  <TextFormat></TextFormat>
  <StringFormat></StringFormat>
  <Animation Value="" />
  <AnimationColor></AnimationColor>
  <Speed></Speed>
</MyObject>
```

## Описание ProgressBar <a href="#description" id="description"></a>

```xml
<MyObject Name="ProgressBarName" Type="ProgressBar" Assembly="BaseControls">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для ProgressBar-->
</MyObject>
```

Значением ProgressBar считается текст, указанный в поле.

### Получение значения <a href="#get-value" id="get-value"></a>

Для получения указанного в поле текста используется get-проперти [Value](progress_bar.md#get_value):

```xml
<Object Name="ProgressBarName">
  <Property Name="Value" />
</Object>
```

Рекомендуется использовать сокращенный вариант записи:

```xml
<Object Name="ProgressBarName" />
```

### Задание значения <a href="#set-value" id="set-value"></a>

Для задания значения текстовому полю используется set-проперти [Value](progress_bar.md#set_value):

```xml
<Object Name="ProgressBarName">
  <Property Name="Value">10</Property>
</Object>
```

Рекомендуется использовать сокращенный вариант записи:

```xml
<Object Name="ProgressBarName">10</Object>
```

## Тэги, специфичные для ProgressBar <a href="#specific-tags" id="specific-tags"></a>

### Custom <a href="#custom" id="custom"></a>

Признак, включающий возможность настраивать стиль прогресс бара. Если признак имеет значение False, то для внешнего вида прогресс бара используются настройки операционной системы.

Необязательный тэг. Значение тэга не ожидается.

Необязательный атрибут `Value` ожидает логическое значение. По умолчанию используется значение False.

```xml
<Custom Value="True" />
```

### Value <a href="#value" id="value"></a>

Задает текущее значение прогресс бара.

Необязательный тэг. Ожидается положительное целочисленное значение.

По умолчанию используется значение 0.

```xml
<Value>0</Value>
```

### Maximum <a href="#maximum" id="maximum"></a>

Задает максимальное значение прогресс бара.

Необязательный тэг. Ожидается положительное целочисленное значение.

По умолчанию используется значение 100.

```xml
<Maximum>200</Maximum>
```

### Minimum <a href="#minimum" id="minimum"></a>

Задает минимальное значение прогресс бара.

Необязательный тэг. Ожидается положительное целочисленное значение.

По умолчанию используется значение 0.

```xml
<Minimum>0</Minimum>
```

### BorderColor <a href="#border_color" id="border_color"></a>

Задает цвет границы прогресс бара.\
Используется, только если тэг [`<Custom>`](progress_bar.md#custom) имеет значение True.

Необязательный тег. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется черный цвет.

```xml
<BorderColor>#FF9800</BorderColor>
```

### BorderWidth <a href="#border_width" id="border_width"></a>

Задает толщину границы прогресс бара.\
Используется, только если тэг [`<Custom>`](progress_bar.md#custom) имеет значение True.

Необязательный тэг. Ожидается положительное целочисленное значение.

По умолчанию используется значение 0.

```xml
<BorderWidth>2</BorderWidth>
```

### ChannelHeight <a href="#channel_height" id="channel_height"></a>

Задает высоту канала.\
Используется, только если тэг [`<Custom>`](progress_bar.md#custom) имеет значение True.

Необязательный тэг. Ожидается положительное целочисленное значение.

По умолчанию используется значение 35

```xml
<ChannelHeight>40</ChannelHeight>
```

### ChannelGradient <a href="#channel_gradient" id="channel_gradient"></a>

Признак, включающий градиентную заливку фона канала.\
Используется, только если тэг [`<Custom>`](progress_bar.md#custom) имеет значение True.

&#x20;Необязательный тэг. Ожидается логическое значение:

<table data-header-hidden><thead><tr><th width="198.926508301592" align="center"></th><th width="355.0302460949434"></th></tr></thead><tbody><tr><td align="center">True</td><td>Градиентная заливка фона канала.<br>Цвета задаются в тэгах <a href="progress_bar.md#channel_first_color"><code>&#x3C;ChannelFirstColor></code></a> и <a href="progress_bar.md#channel_second_color"><code>&#x3C;ChannelSecondColor></code></a>.</td></tr><tr><td align="center">False</td><td>Однотонная заливка фона канала.<br>Цвет задается в тэге <a href="progress_bar.md#channel_first_color"><code>&#x3C;ChannelFirstColor></code></a>.</td></tr></tbody></table>

По умолчанию используется значение False.

```xml
<ChannelGradient>True</ChannelGradient>
```

### ChannelFirstColor <a href="#channel_first_color" id="channel_first_color"></a>

Задает основной цвет канала.\
Используется, только если тэг [`<Custom>`](progress_bar.md#custom) имеет значение True.

Необязательный тег. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется Transparent

```xml
<ChannelFirstColor>#757575</ChannelFirstColor>
```

### ChannelSecondColor <a href="#channel_second_color" id="channel_second_color"></a>

Задает второй цвет канала.\
Используется, только если тэг [`<Custom>`](progress_bar.md#custom) имеет значение True, и свойству [ChannelGradient](progress_bar.md#channel_gradient) задано значение True.

Необязательный тег. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется Gray

```xml
<ChannelSecondColor>#9E9E9E</ChannelSecondColor>
```

### SliderHeight <a href="#slider_height" id="slider_height"></a>

Задает высоту слайдера.\
Используется, только если тэг [`<Custom>`](progress_bar.md#custom) имеет значение True.

Необязательный тэг. Ожидается положительное целочисленное значение.

По умолчанию используется значение 35

```xml
<SliderHeight>40</SliderHeight>
```

### SliderGradient <a href="#slider_gradient" id="slider_gradient"></a>

Признак, включающий градиентную заливку слайдера.\
Используется, только если тэг [`<Custom>`](progress_bar.md#custom) имеет значение True.

Необязательный тэг. Ожидается логическое значение:

<table data-header-hidden><thead><tr><th width="198.926508301592" align="center"></th><th width="355.0302460949434"></th></tr></thead><tbody><tr><td align="center">True</td><td>Градиентная заливка слайдера.<br>Цвета задаются в тэгах <a href="progress_bar.md#slider_first_color"><code>&#x3C;SliderFirstColor></code></a> и <a href="progress_bar.md#slider_second_color"><code>&#x3C;SliderSecondColor></code></a>.</td></tr><tr><td align="center">False</td><td>Однотонная заливка слайдера.<br>Цвет задается в тэге <a href="progress_bar.md#slider_first_color"><code>&#x3C;SliderFirstColor></code></a>.</td></tr></tbody></table>

По умолчанию используется значение False.

```xml
<SliderGradient>True</SliderGradient>
```

### SliderFirstColor <a href="#slider_first_color" id="slider_first_color"></a>

Задает основной цвет слайдера.\
Используется, только если тэг [`<Custom>`](progress_bar.md#custom) имеет значение True.

Необязательный тег. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется LightGreen

```xml
<SliderFirstColor>#689F38</SliderFirstColor>
```

### SliderSecondColor <a href="#slider_second_color" id="slider_second_color"></a>

Задает второй цвет слайдера.\
Используется, только если тэг [`<Custom>`](progress_bar.md#custom) имеет значение True, и свойству [SliderGradient](progress_bar.md#slider_gradient) задано значение True.

Необязательный тег. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется YellowGreen

```xml
<SliderSecondColor>#CDDC39</SliderSecondColor>
```

### TextAlign <a href="#text_align" id="text_align"></a>

Используется, чтобы указать способ выравнивания текста по горизонтали.\
Используется, только если тэг [`<Custom>`](progress_bar.md#custom) имеет значение True.

Необязательный тэг. Ожидается название одного из способов выравнивания текста по горизонтали.:

<table data-header-hidden><thead><tr><th width="198.926508301592" align="center"></th><th width="355.0302460949434"></th></tr></thead><tbody><tr><td align="center">TopLeft</td><td>Слева сверху</td></tr><tr><td align="center">TopCenter</td><td>По центру сверху</td></tr><tr><td align="center">TopRight</td><td>Справа сверху</td></tr><tr><td align="center">MiddleLeft</td><td>Слева посередине</td></tr><tr><td align="center">MiddleCenter</td><td>По центру посередине</td></tr><tr><td align="center">MiddleRight</td><td>Справа посередине</td></tr><tr><td align="center">Slide</td><td>Плывущий по верху текст</td></tr><tr><td align="center">None</td><td>Текст отсутствует</td></tr></tbody></table>

По умолчанию используется значение None.

```xml
<TextAlign>MiddleCenter</TextAlign>
```

### TextFormat <a href="#text_format" id="text_format"></a>

Задает название формата отображения текста.\
Используется, только если тэг [`<Custom>`](progress_bar.md#custom) имеет значение True, а свойство [TextAlign](progress_bar.md#text_align) имеет значение отличное от None.

Необязательный тэг. Ожидается название одного из типов положения текста:

<table data-header-hidden><thead><tr><th width="329.6076612093773" align="center"></th><th width="355.0302460949434"></th></tr></thead><tbody><tr><td align="center">Percentage</td><td>Отображается текущее значение в виде процентов, рассчитанных по формуле: Value/Maximum * 100</td></tr><tr><td align="center">Value</td><td>Отображается текущее значение прогресс бара.</td></tr><tr><td align="center">ValueOverMaximum</td><td>Отображается строка вида: Value/Maximum</td></tr><tr><td align="center">Text</td><td>Формат строки задается в тэге <code>&#x3C;StringFormat></code></td></tr></tbody></table>

По умолчанию принимает значение Value.

```xml
<TextFormat>ValueOverMaximum</TextFormat>
```

### StringFormat <a href="#string_format" id="string_format"></a>

Задает шаблон строки для отображаемого текста.\
Используется, только если тэг [`<Custom>`](progress_bar.md#custom) имеет значение True, а тэг [`<TextFormat>`](progress_bar.md#text_format) - значение Text.

Необязательный тэг. Любое значение будет переведено в текстовое.

Поддерживает две переменные для получения собственных свойств: {0} - Value, {1} - Maximum.

```xml
<StringFormat>{0} из {1}</StringFormat>
```

### Animation

Признак, включающий анимацию при заполнении прогресс бара.\
Используется только если тэг [`<Custom>`](progress_bar.md#custom) имеет значение True.

Необязательный тэг. Значение тэга не ожидается.

Необязательный атрибут `Value` ожидает логическое значение. По умолчанию используется значение False.

```xml
<Animation Value="True" />
```

### AnimationColor <a href="#animation_color" id="animation_color"></a>

Задает цвет анимации.\
Используется, только если тэг [`<Custom>`](progress_bar.md#custom) имеет значение True и анимация прогресс бара включена.

Необязательный тег. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется YellowGreen.

```xml
<AnimationColor>#CDDC39</AnimationColor>
```

### Speed <a href="#speed" id="speed"></a>

Задает скорость анимации.\
Используется только если тэг [`<Custom>`](progress_bar.md#custom) имеет значение True и анимация прогресс бара включена.

Необязательный тэг. Ожидается положительное целочисленное значение.

По умолчанию используется значение 2.

```xml
<Speed>2</Speed>
```

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### Value <a href="#get_value" id="get_value"></a>

Возвращает текущее значение прогресс бара.

```xml
<Object Name="ProgressBarName">
  <Property Name="Value" />
</Object>
```

### Maximum <a href="#get_maximum" id="get_maximum"></a>

Возвращает максимальное значение прогресс бара.

```xml
<Object Name="ProgressBarName">
  <Property Name="Maximum" />
</Object>
```

### Minimum <a href="#get_minimum" id="get_minimum"></a>

Возвращает минимальное значение прогресс бара

```xml
<Object Name="ProgressBarName">
  <Property Name="Minimum" />
</Object>
```

### BorderColor <a href="#get_border_color" id="get_border_color"></a>

Возвращает цвет границы прогресс бара.

```xml
<Object Name="ProgressBarName">
  <Property Name="BorderColor" />
</Object>
```

### BorderWidth <a href="#get_border_width" id="get_border_width"></a>

Возвращает толщину границы прогресс бара.

```xml
<Object Name="ProgressBarName">
  <Property Name="BorderWidth" />
</Object>
```

### ChannelHeight <a href="#get_channel_height" id="get_channel_height"></a>

Возвращает высоту канала.

```xml
<Object Name="ProgressBarName">
  <Property Name="ChannelHeight" />
</Object>
```

### ChannelGradient <a href="#get_channel_gradient" id="get_channel_gradient"></a>

Возвращает тип заливки фона канала.

```xml
<Object Name="ProgressBarName">
  <Property Name="ChannelGradient" />
</Object>
```

### ChannelFirstColor <a href="#get_channel_first_color" id="get_channel_first_color"></a>

Возвращает основной цвет канала.

```xml
<Object Name="ProgressBarName">
  <Property Name="ChannelFirstColor" />
</Object>
```

### ChannelSecondColor <a href="#get_channel_second_color" id="get_channel_second_color"></a>

Возвращает второй цвет канала.

```xml
<Object Name="ProgressBarName">
  <Property Name="ChannelSecondColor" />
</Object>
```

### SliderHeight <a href="#get_slider_height" id="get_slider_height"></a>

Возвращает высоту слайдера.

```xml
<Object Name="ProgressBarName">
  <Property Name="SliderHeight" />
</Object>
```

### SliderGradient <a href="#get_slider_gradient" id="get_slider_gradient"></a>

Возвращает типа заливки слайдера.

```xml
<Object Name="ProgressBarName">
  <Property Name="SliderGradient" />
</Object>
```

### SliderFirstColor <a href="#get_slider_first_color" id="get_slider_first_color"></a>

Возвращает основной цвет слайдера.

```xml
<Object Name="ProgressBarName">
  <Property Name="SliderFirstColor" />
</Object>
```

### SliderSecondColor <a href="#get_slider_second_color" id="get_slider_second_color"></a>

Возвращает второй цвет слайдера.

```xml
<Object Name="ProgressBarName">
  <Property Name="SliderSecondColor" />
</Object>
```

### TextAlign <a href="#get_text_align" id="get_text_align"></a>

Возвращает название способа выравнивания текста по горизонтали.

```xml
<Object Name="ProgressBarName">
  <Property Name="TextAlign" />
</Object>
```

### TextFormat <a href="#get_text_format" id="get_text_format"></a>

Возвращает название типа формата отображаемого текста.

```xml
<Object Name="ProgressBarName">
  <Property Name="TextFormat" />
</Object>
```

### StringFormat <a href="#get_string_format" id="get_string_format"></a>

Возвращает шаблон строки отображаемого текста.

```xml
<Object Name="ProgressBarName">
  <Property Name="StringFormat" />
</Object>
```

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

### Value <a href="#set_value" id="set_value"></a>

Задает текущее значение прогресс бара.

Ожидается положительное целочисленное значение.

```xml
<Object Name="ProgressBarName">
  <Property Name="Value">10</Property>
</Object>
```

### Maximum <a href="#set_maximum" id="set_maximum"></a>

Задает максимальное значение прогресс бара.

Ожидается положительное целочисленное значение.

```xml
<Object Name="ProgressBarName">
  <Property Name="Maximum">200</Property>
</Object>
```
