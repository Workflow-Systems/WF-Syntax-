---
description: >-
  Ползунок для задания значения в допустимом интервале. Элемент
  пользовательского интерфейса.
---

# Slider

## Шаблон Slider <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="SliderName" Type="Slider" Assembly="BaseControls">
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
  <!--Тэги, специфичные для Slider-->
  <Value></Value>
  <Minimum></Minimum>
  <Maximum></Maximum>
  <Orientation></Orientation>
  <ColorSchema Value="" >
    <LineColor></LineColor>
    <ThumbFirstColor></ThumbFirstColor>
    <ThumbSecondColor></ThumbSecondColor>
    <ThumbBorderColor></ThumbBorderColor>
    <BarFirstColor></BarFirstColor>
    <BarSecondColor></BarSecondColor>
    <BarThirdColor></BarThirdColor>
    <ElapsedFirstColor></ElapsedFirstColor>
    <ElapsedSecondColor></ElapsedSecondColor>
    <ElapsedThirdColor></ElapsedThirdColor>
  </ColorSchema>
  <ThumbWidth></ThumbWidth>
  <ThumbHeight></ThumbHeight>
  <ThumbRound></ThumbRound>
  <Padding></Padding>
  <StepSize></StepSize>
  <LineMarkAlign></LineMarkAlign>
  <LineSegmentQuantity></LineSegmentQuantity>
  <LineSubSegmentQuantity></LineSubSegmentQuantity>
  <TypeLineText></TypeLineText>
  <DrawSemitransparentThumb></DrawSemitransparentThumb>
  <IsMouseEffect></IsMouseEffect>
</MyObject>
```

## Описание Slider <a href="#description" id="description"></a>

```xml
<MyObject Name="SliderName" Type="Slider" Assembly="BaseControls">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для Slider-->
</MyObject>
```

Значением Slider считается текст, указанный в поле.

### Получение значения <a href="#get-value" id="get-value"></a>

Для получения указанного в поле текста используется get-проперти [Value](./#get_value):

```xml
<Object Name="SliderName">
  <Property Name="Value" />
</Object>
```

Рекомендуется использовать сокращенный вариант записи:

```xml
<Object Name="SliderName" />
```

### Задание значения <a href="#set-value" id="set-value"></a>

Для задания значения текстовому полю используется set-проперти [Value](./#set_value):

```xml
<Object Name="SliderName">
  <Property Name="Value">10</Property>
</Object>
```

Рекомендуется использовать сокращенный вариант записи:

```xml
<Object Name="SliderName">10</Object>
```

## Тэги, специфичные для Slider <a href="#specific-tags" id="specific-tags"></a>

### Value <a href="#value" id="value"></a>

Задает текущее значение ползунка.

Необязательный тэг. Ожидается положительное целочисленное значение.

По умолчанию используется значение 0.

```xml
<Value>0</Value>
```

### Minimum <a href="#minimum" id="minimum"></a>

Задает минимальное значение ползунка.

Необязательный тэг. Ожидается положительное целочисленное значение.

По умолчанию используется значение 0.

```xml
<Minimum>0</Minimum>
```

### Maximum <a href="#maximum" id="maximum"></a>

Задает максимальное значение ползунка.

Необязательный тэг. Ожидается положительное целочисленное значение.

По умолчанию используется значение 100.

```xml
<Maximum>200</Maximum>
```

### Orientation <a href="#orientation" id="orientation"></a>

Ориентация бегунка.

Необязательный тэг. Ожидается название одного из типов ориентации бегунка:

<table data-header-hidden><thead><tr><th width="200"></th><th></th></tr></thead><tbody><tr><td>Horizontal</td><td>Горизонтальная ориентация бегунка</td></tr><tr><td>Vertical</td><td>Вертикальная ориентация бегунка</td></tr></tbody></table>

По умолчанию используется значение Horizontal.

```xml
<Orientation>Vertical</Orientation>
```

### ColorSchema <a href="#color_schema" id="color_schema"></a>

Задает цветовую схему, предопределенную в платформе. \
Схема задается через необязательный атрибут `Value`. Отдельные цвета в выбранной схеме можно изменять через вложенные тэги.

Необязательный тэг. Описание вложенных тэгов по [ссылке](color_schema.md).

```xml
<ColorSchema Value="Red">
  <LineColor>LineColorName</LineColor>
  <ThumbFirstColor>ThumbFirstColorName</ThumbFirstColor>
  <ThumbSecondColor>ThumbSecondColorName</ThumbSecondColor>
  <ThumbBorderColor>ThumbBorderColorName</ThumbBorderColor>
  <BarFirstColor>BarFirstColorName</BarFirstColor>
  <BarSecondColor>BarSecondColorName</BarSecondColor>
  <BarThirdColor>BarThirdColorName</BarThirdColor>
  <ElapsedFirstColor>ElapsedFName</ElapsedFirstColor>
  <ElapsedSecondColor>ElapsedSecondColorName</ElapsedSecondColor>
  <ElapsedThirdColor>ElapsedThirdName</ElapsedThirdColor>
</ColorSchema>
```

### ThumbWidth <a href="#thumb_width" id="thumb_width"></a>

Ширина бегунка.

Необязательный тэг. Ожидается положительное целочисленное значение.

По умолчанию используется значение 16.

```xml
<ThumbWidth>20</ThumbWidth>
```

### ThumbHeight <a href="#thumb_height" id="thumb_height"></a>

Высота бегунка.

Необязательный тэг. Ожидается положительное целочисленное значение.

По умолчанию используется значение 16.

```xml
<ThumbHeight>20</ThumbHeight>
```

### ThumbRound <a href="#thumb_round" id="thumb_round"></a>

Сила закругления прямоугольника бегунка.

Необязательный тэг. Ожидается положительное целочисленное значение.

По умолчанию используется значение 16.

```xml
<ThumbRound>10</ThumbRound>
```

### Padding <a href="#padding" id="padding"></a>

Внутренний отступ от краёв объекта.

Необязательный тэг. Ожидается положительное целочисленное значение.

По умолчанию используется значение 5.

```xml
<Padding>5</Padding>
```

### StepSize <a href="#step_size" id="step_size"></a>

Число, на которое будет изменяться значение поля.

Необязательный тэг. Ожидается положительное целочисленное значение.

По умолчанию используется значение 1.

```xml
<Step>5</Step>
```

### LineMarkAlign <a href="#line_mark_align" id="line_mark_align"></a>

Наличие и тип меток на линейке.

Необязательный тэг. Ожидается название одного из типов меток:

<table data-header-hidden><thead><tr><th width="200"></th><th></th></tr></thead><tbody><tr><td>None</td><td>Метки отсутствуют.</td></tr><tr><td>Top</td><td>Если свойство <a href="./#orientation"><code>Orientation</code></a> имеет значение Horizontal, то метки отображаются над линейкой.<br>Если свойство <a href="./#orientation"><code>Orientation</code></a> имеет значение Vertical, то метки отображаются слева от линейки.</td></tr><tr><td>Bottom</td><td>Если свойство <a href="./#orientation"><code>Orientation</code></a> имеет значение Horizontal, то метки отображаются под линейкой.<br>Если свойство <a href="./#orientation"><code>Orientation</code></a> имеет значение Vertical, то метки отображаются справа от линейки.</td></tr><tr><td>All</td><td>Метки отображаются с обеих сторон от линейки.</td></tr></tbody></table>

По умолчанию используется значение Bottom.

```xml
<LineMarkAlign>Bottom</LineMarkAlign>
```

### LineSegmentQuantity <a href="#line_segment_quantity" id="line_segment_quantity"></a>

Количество больших засечек на баре.

Необязательный тэг. Ожидается положительное целочисленное значение.

По умолчанию используется значение 10.

```xml
<LineSegmentQuantity>10</LineSegmentQuantity>
```

### LineSubSegmentQuantity <a href="#line_subsegment_quantity" id="line_subsegment_quantity"></a>

Количество маленьких засечек между большими.

Необязательный тэг. Ожидается положительное целочисленное значение.

По умолчанию используется значение 2.

```xml
<LineSubSegmentQuantity>2</LineSubSegmentQuantity>
```

### TypeLineText <a href="#type_line_text" id="type_line_text"></a>

Задает тип отображения цифр над делениями.

Необязательный тэг. Ожидается название одного из типов отображения:

<table data-header-hidden><thead><tr><th width="40"></th><th></th></tr></thead><tbody><tr><td>Default</td><td>В виде десятичной дроби.</td></tr><tr><td>SimpleFraction</td><td>В виде простой дроби.</td></tr><tr><td>None</td><td>Цифры над делениями отсутствуют.</td></tr></tbody></table>

По умолчанию используется значение Default.

```xml
<TypeLineText>SimpleFraction</TypeLineText>
```

### DrawSemitransparentThumb <a href="#draw_semitransparent_thumb" id="draw_semitransparent_thumb"></a>

Признак полупрозрачности бегунка при захвате мышкой.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<DrawSemitransparentThumb>True</DrawSemitransparentThumb>
```

### IsMouseEffect <a href="#is_mouse_effect" id="is_mouse_effect"></a>

Признак подсветки слайдер, при наведении мышки.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение True.

```xml
<IsMouseEffect>False</IsMouseEffect>
```

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### Value <a href="#get_value" id="get_value"></a>

Возвращает текущее значение ползунка.

```xml
<Object Name="SliderName">
  <Property Name="Value" />
</Object>
```

### Minimum <a href="#get_minimum" id="get_minimum"></a>

Возвращает минимальное значение ползунка.

```xml
<Object Name="SliderName">
  <Property Name="Minimum" />
</Object>
```

### Maximum <a href="#get_maximum" id="get_maximum"></a>

Возвращает максимальное значение ползунка.

```xml
<Object Name="SliderName">
  <Property Name="Maximum" />
</Object>
```

### Orientation <a href="#get_orientation" id="get_orientation"></a>

Возвращает название типа ориентации бегунка.

```xml
<Object Name="SliderName">
  <Property Name="Orientation" />
</Object>
```

### ThumbWidth <a href="#get_thumb_width" id="get_thumb_width"></a>

Возвращает значение ширины бегунка.

```xml
<Object Name="SliderName">
  <Property Name="ThumbWidth" />
</Object>
```

### ThumbHeight <a href="#get_thumb_height" id="get_thumb_height"></a>

Возвращает значение высоты бегунка.

```xml
<Object Name="SliderName">
  <Property Name="ThumbHeight" />
</Object>
```

### ThumbRound <a href="#get_thumb_round" id="get_thumb_round"></a>

Возвращает значение силы закругления прямоугольника бегунка.

```xml
<Object Name="SliderName">
  <Property Name="ThumbRound" />
</Object>
```

### Padding <a href="#get_padding" id="get_padding"></a>

Возвращает значение внутреннего отступа от краёв объекта.

```xml
<Object Name="SliderName">
  <Property Name="Padding" />
</Object>
```

### StepSize <a href="#get_step_size" id="get_step_size"></a>

Возвращает число, на которое будет изменяться значение поля.

```xml
<Object Name="SliderName">
  <Property Name="StepSize" />
</Object>
```

### LineMarkAlign <a href="#get_line_mark_align" id="get_line_mark_align"></a>

Возвращает наличие и тип меток на линейке.

```xml
<Object Name="SliderName">
  <Property Name="LineMarkAlign" />
</Object>
```

### LineSegmentQuantity <a href="#get_line_segment_quantity" id="get_line_segment_quantity"></a>

Возвращает количество больших засечек на баре.

```xml
<Object Name="SliderName">
  <Property Name="LineSegmentQuantity" />
</Object>
```

### LineSubSegmentQuantity <a href="#get_line_subsegment_quantity" id="get_line_subsegment_quantity"></a>

Возвращает количество маленьких засечек между большими.

```xml
<Object Name="SliderName">
  <Property Name="LineSubSegmentQuantity" />
</Object>
```

### TypeLineText <a href="#get_type_line_text" id="get_type_line_text"></a>

Возвращает тип отображения цифр над делениями.

```xml
<Object Name="SliderName">
  <Property Name="TypeLineText" />
</Object>
```

### DrawSemitransparentThumb <a href="#get_draw_semitransparent_thumb" id="get_draw_semitransparent_thumb"></a>

Возвращает признак полупрозрачности бегунка при захвате мышкой.

```xml
<Object Name="SliderName">
  <Property Name="Maximum" />
</Object>
```

### IsMouseEffect <a href="#get_is_mouse_effect" id="get_is_mouse_effect"></a>

Возвращает признак подсветки слайдер, при наведении мышки.

```xml
<Object Name="SliderName">
  <Property Name="IsMouseEffect" />
</Object>
```

### LineColor <a href="#get_line_color" id="get_line_color"></a>

Возвращает цвет делений на шкале.

```xml
<Object Name="SliderName">
  <Property Name="LineColor" />
</Object>
```

### ThumbFirstColor <a href="#get_thumb_first_color" id="get_thumb_first_color"></a>

Возвращает первый цвет бегунка (сверху вниз, слева направо).

```xml
<Object Name="SliderName">
  <Property Name="IsMouseEffect" />
</Object>
```

### ThumbSecondColor <a href="#get_thumb_second_color" id="get_thumb_second_color"></a>

Возвращает второй цвет бегунка (сверху вниз, слева направо).

```xml
<Object Name="SliderName">
  <Property Name="IsMouseEffect" />
</Object>
```

### ThumbBorderColor <a href="#get_thumb_border_color" id="get_thumb_border_color"></a>

Возвращает цвет границы бегунка.

```xml
<Object Name="SliderName">
  <Property Name="IsMouseEffect" />
</Object>
```

### BarFirstColor <a href="#get_bar_first_color" id="get_bar_first_color"></a>

Возвращает первый цвет бара (сверху вниз, слева направо).

```xml
<Object Name="SliderName">
  <Property Name="IsMouseEffect" />
</Object>
```

### BarSecondColor <a href="#get_bar_second_color" id="get_bar_second_color"></a>

Возвращает второй цвет бара (сверху вниз, слева направо).

```xml
<Object Name="SliderName">
  <Property Name="IsMouseEffect" />
</Object>
```

### BarThirdColor <a href="#get_bar_third_color" id="get_bar_third_color"></a>

Возвращает третий цвет бара (сверху вниз, слева направо).

```xml
<Object Name="SliderName">
  <Property Name="IsMouseEffect" />
</Object>
```

### ElapsedFirstColor <a href="#get_elapsed_first_color" id="get_elapsed_first_color"></a>

Возвращает первый цвет заполненной шкалы (сверху вниз, слева направо).

```xml
<Object Name="SliderName">
  <Property Name="IsMouseEffect" />
</Object>
```

### ElapsedSecondColor <a href="#get_elapsed_second_color" id="get_elapsed_second_color"></a>

Возвращает второй цвет заполненной шкалы (сверху вниз, слева направо).

```xml
<Object Name="SliderName">
  <Property Name="IsMouseEffect" />
</Object>
```

### ElapsedThirdColor <a href="#get_elapsed_third_color" id="get_elapsed_third_color"></a>

Возвращает третий цвет заполненной шкалы (сверху вниз, слева направо).

```xml
<Object Name="SliderName">
  <Property Name="IsMouseEffect" />
</Object>
```

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

### Value <a href="#set_value" id="set_value"></a>

Задает текущее значение ползунка.

Ожидается положительное целочисленное значение.

```xml
<Object Name="SliderName">
  <Property Name="Value">20</Property>
</Object>
```

### Minimum <a href="#set_minimum" id="set_minimum"></a>

Задает минимальное значение ползунка.

Ожидается положительное целочисленное значение.

```xml
<Object Name="SliderName">
  <Property Name="Minimum">10</Property>
</Object>
```

### Maximum <a href="#set_maximum" id="set_maximum"></a>

Задает максимальное значение ползунка.

Ожидается положительное целочисленное значение.

```xml
<Object Name="SliderName">
  <Property Name="Maximum">200</Property>
</Object>
```

### Orientation <a href="#set_orientation" id="set_orientation"></a>

Задает название типа ориентации бегунка.

Ожидается одно из допустимых значений, указанных в описании тэга [`<Orientation>`](./#orientation).

```xml
<Object Name="SliderName">
  <Property Name="Orientation">Vertical</Property>
</Object>
```

### ThumbWidth <a href="#set_thumb_width" id="set_thumb_width"></a>

Задает ширину бегунка.

Ожидается положительное целочисленное значение.

```xml
<Object Name="SliderName">
  <Property Name="ThumbWidth">16</Property>
</Object>
```

### ThumbHeight <a href="#set_thumb_height" id="set_thumb_height"></a>

Задает высоту бегунка.

Ожидается положительное целочисленное значение.

```xml
<Object Name="SliderName">
  <Property Name="ThumbHeight">16</Property>
</Object>
```

### ThumbRound <a href="#set_thumb_round" id="set_thumb_round"></a>

Задает силу закругления прямоугольника бегунка.

Ожидается положительное целочисленное значение.

```xml
<Object Name="SliderName">
  <Property Name="ThumbRound">16</Property>
</Object>
```

### Padding <a href="#set_padding" id="set_padding"></a>

Задает внутренний отступ от краёв объекта.

Ожидается положительное целочисленное значение.

```xml
<Object Name="SliderName">
  <Property Name="Padding">5</Property>
</Object>
```

### StepSize <a href="#set_step_size" id="set_step_size"></a>

Задает число, на которое будет изменяться значение поля.

Ожидается положительное целочисленное значение.

```xml
<Object Name="SliderName">
  <Property Name="StepSize">5</Property>
</Object>
```

### LineMarkAlign <a href="#set_line_mark_align" id="set_line_mark_align"></a>

Задает наличие и тип меток на линейке.

Ожидается одно из допустимых значений, указанных в описании тэга [`<LineMarkAlign>`](./#line_mark_align).

```xml
<Object Name="SliderName">
  <Property Name="LineMarkAlign">Top</Property>
</Object>
```

### LineSegmentQuantity <a href="#set_line_segment_quantity" id="set_line_segment_quantity"></a>

Задает количество больших засечек на баре.

Ожидается положительное целочисленное значение.

```xml
<Object Name="SliderName">
  <Property Name="LineSegmentQuantity">10</Property>
</Object>
```

### LineSubSegmentQuantity <a href="#set_line_subsegment_quantity" id="set_line_subsegment_quantity"></a>

Задает количество маленьких засечек между большими.

Ожидается положительное целочисленное значение.

```xml
<Object Name="SliderName">
  <Property Name="LineSubSegmentQuantity">3</Property>
</Object>
```

### TypeLineText <a href="#set_type_line_text" id="set_type_line_text"></a>

Задает тип отображения цифр над делениями.

Ожидается одно из допустимых значений, указанных в описании тэга [`<TypeLineText>`](./#type_line_text).

```xml
<Object Name="SliderName">
  <Property Name="TypeLineText">SimpleFraction</Property>
</Object>
```

### DrawSemitransparentThumb <a href="#set_draw_semitransparent_thumb" id="set_draw_semitransparent_thumb"></a>

Задает признак полупрозрачности бегунка при захвате мышкой.

Ожидается логическое значение.

```xml
<Object Name="SliderName">
  <Property Name="Maximum">True</Property>
</Object>
```

### IsMouseEffect <a href="#set_is_mouse_effect" id="set_is_mouse_effect"></a>

Задает признак подсветки слайдер, при наведении мышки.

Ожидается логическое значение.

```xml
<Object Name="SliderName">
  <Property Name="IsMouseEffect">False</Property>
</Object>
```

### LineColor <a href="#set_line_color" id="set_line_color"></a>

Задает цвет делений на шкале.

Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

```xml
<Object Name="SliderName">
  <Property Name="LineColor">LineColorName</Property>
</Object>
```

### ThumbFirstColor <a href="#set_thumb_first_color" id="set_thumb_first_color"></a>

Задает первый цвет бегунка (сверху вниз, слева направо).

Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

```xml
<Object Name="SliderName">
  <Property Name="IsMouseEffect">ThumbFirstColorName</Property>
</Object>
```

### ThumbSecondColor <a href="#set_thumb_second_color" id="set_thumb_second_color"></a>

Задает второй цвет бегунка (сверху вниз, слева направо).

Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

```xml
<Object Name="SliderName">
  <Property Name="IsMouseEffect">ThumbSecondColorName</Property>
</Object>
```

### ThumbBorderColor <a href="#set_thumb_border_color" id="set_thumb_border_color"></a>

Задает цвет границы бегунка.

Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

```xml
<Object Name="SliderName">
  <Property Name="IsMouseEffect">ThumbBorderColorName</Property>
</Object>
```

### BarFirstColor <a href="#set_bar_first_color" id="set_bar_first_color"></a>

Задает первый цвет бара (сверху вниз, слева направо).

Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

```xml
<Object Name="SliderName">
  <Property Name="IsMouseEffect">BarFirstColorName</Property>
</Object>
```

### BarSecondColor <a href="#set_bar_second_color" id="set_bar_second_color"></a>

Задает второй цвет бара (сверху вниз, слева направо).

Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

```xml
<Object Name="SliderName">
  <Property Name="IsMouseEffect">BarSecondColorName</Property>
</Object>
```

### BarThirdColor <a href="#set_bar_third_color" id="set_bar_third_color"></a>

Задает третий цвет бара (сверху вниз, слева направо).

Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

```xml
<Object Name="SliderName">
  <Property Name="IsMouseEffect">BarThirdColorName</Property>
</Object>
```

### ElapsedFirstColor <a href="#set_elapsed_first_color" id="set_elapsed_first_color"></a>

Задает первый цвет заполненной шкалы (сверху вниз, слева направо).

Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

```xml
<Object Name="SliderName">
  <Property Name="IsMouseEffect">ElapsedFirstColorName</Property>
</Object>
```

### ElapsedSecondColor <a href="#set_elapsed_second_color" id="set_elapsed_second_color"></a>

Задает второй цвет заполненной шкалы (сверху вниз, слева направо).

Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

```xml
<Object Name="SliderName">
  <Property Name="IsMouseEffect">ElapsedSecondColorName</Property>
</Object>
```

### ElapsedThirdColor <a href="#set_elapsed_third_color" id="set_elapsed_third_color"></a>

Задает третий цвет заполненной шкалы (сверху вниз, слева направо).

Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

```xml
<Object Name="SliderName">
  <Property Name="IsMouseEffect">ElapsedThirdColorName</Property>
</Object>
```
