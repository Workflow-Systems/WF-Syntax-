---
description: Графический объект; анимация.
---

# Spinner

## Шаблон Spinner <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="" Type="Spinner" Assembly="BaseControls" ChangeForm="">
  <!--Тэги, общие для всех графических объектов-->
  <Top></Top>
  <Bottom></Bottom>
  <Left></Left>
  <Right></Right>
  <Left></Left>
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
  <!--Тэги, специфичные для Spinner-->
  <BarCount></BarCount>
  <BarWidth></BarWidth>
  <BarHeight></BarHeight>
  <InnerRadius></InnerRadius>
  <OuterRadius></OuterRadius>
  <ColorA></ColorA>
  <ColorB></ColorB>
</MyObject>
```

## Описание Spinner <a href="#description" id="description"></a>

```xml
<MyObject Name="SpinnerName" Type="Spinner" Assembly="BaseControls">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для Spinner-->
</MyObject>
```

Spinner не имеет значения.

## Тэги, специфичные для Spinner <a href="#specific-tags" id="specific-tags"></a>

### BarCount <a href="#bar_count" id="bar_count"></a>

Количество полос.

Необязательный тэг. Ожидается целочисленное значение.

Если тэг `<BarCount>` отсутствует, то используется значение 16.

```xml
<BarCount>16</BarCount>
```

### BarWidth <a href="#bar_width" id="bar_width"></a>

Ширина полосы.

Необязательный тэг. Ожидается числовое значение.

Если тэг `<BarWidth>` отсутствует, то используется значение 2.5.

```xml
<BarWidth>2.5</BarWidth>
```

### BarHeight <a href="#bar_height" id="bar_height"></a>

Высота полосы.

Необязательный тэг. Ожидается числовое значение.

Если тэг `<BarHeight>` отсутствует, то используется значение 15.

```xml
<BarHeight>15</BarHeight>
```

Если тег `<BarHeight>` присутствует вместе с тегом [`<OuterRadius>`](spinner.md#outer_radius), то конфликт разрешается в пользу тега [`<OuterRadius>`](spinner.md#outer_radius).

### InnerRadius <a href="#inner_radius" id="inner_radius"></a>

Внутренний радиус.

Необязательный тэг. Ожидается числовое значение.

Если тэг `<InnerRadius>` отсутствует, то используется значение 10.

```xml
<InnerRadius>10</InnerRadius>
```

### OuterRadius <a href="#outer_radius" id="outer_radius"></a>

Внешний радиус.

Необязательный тэг. Ожидается числовое значение.

Если тэг `<OuterRadius>` отсутствует, то используется значение 25.

```xml
<OuterRadius>25</OuterRadius>
```

Если тег `<OuterRadius>` присутствует вместе с тегом [`<BarHeight>`](spinner.md#bar_height), то конфликт разрешается в пользу тега `<OuterRadius>`.

### ColorA <a href="#color_a" id="color_a"></a>

Название цвета первой полосы.

Необязательный тэг. Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

Если тэг `<ColorA>` отсутствует, то используется значение #000000 ![](https://www.htmlcsscolor.com/preview/icon/000000.png).

```xml
<ColorA>#000000</ColorA>
```

### ColorB <a href="#color_b" id="color_b"></a>

Название цвета последней полосы.

Необязательный тэг. Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

Если тэг `<ColorB>` отсутствует, то используется значение #E6E6E6 ![](https://www.htmlcsscolor.com/preview/icon/E6E6E6.png).

```xml
<ColorB>#E6E6E6</ColorB>
```

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### BarCount <a href="#get_bar_count" id="get_bar_count"></a>

Возвращает количество полос.

```xml
<Object Name="SpinnerName">
  <Property Name="BarCount" />
</Object>
```

### BarWidth <a href="#get_bar_width" id="get_bar_width"></a>

Возвращает ширину полосы.

```xml
<Object Name="SpinnerName">
  <Property Name="BarWidth" />
</Object>
```

### BarHeight <a href="#get_bar_height" id="get_bar_height"></a>

Возвращает высоту полосы.

```xml
<Object Name="SpinnerName">
  <Property Name="BarHeight" />
</Object>
```

### InnerRadius <a href="#get_inner_radius" id="get_inner_radius"></a>

Возвращает внутренний радиус.

```xml
<Object Name="SpinnerName">
  <Property Name="InnerRadius" />
</Object>
```

### OuterRadius <a href="#get_outer_radius" id="get_outer_radius"></a>

Возвращает внешний радиус.

```xml
<Object Name="SpinnerName">
  <Property Name="OuterRadius" />
</Object>
```

### ColorA <a href="#get_color_a" id="get_color_a"></a>

Возвращает название цвета первой полосы.

```xml
<Object Name="SpinnerName">
  <Property Name="ColorA" />
</Object>
```

### ColorB <a href="#get_color_b" id="get_color_b"></a>

Возвращает название цвета последней полосы.

```xml
<Object Name="SpinnerName">
  <Property Name="ColorB" />
</Object>
```

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

### BarCount <a href="#set_bar_count" id="set_bar_count"></a>

Задаёт количество полос.

Ожидается целочисленное значение.

```xml
<Object Name="SpinnerName">
  <Property Name="BarCount">16</Property>
</Object>
```

### BarWidth <a href="#set_bar_width" id="set_bar_width"></a>

Задаёт ширину полосы.

Ожидается числовое значение.

```xml
<Object Name="SpinnerName">
  <Property Name="BarWidth">2.5</Property>
</Object>
```

### BarHeight <a href="#set_bar_height" id="set_bar_height"></a>

Задаёт высоту полосы.

Ожидается числовое значение.

```xml
<Object Name="SpinnerName">
  <Property Name="BarHeight">15</Property>
</Object>
```

### InnerRadius <a href="#set_inner_radius" id="set_inner_radius"></a>

Задаёт внутренний радиус.

Ожидается числовое значение.

```xml
<Object Name="SpinnerName">
  <Property Name="InnerRadius">10</Property>
</Object>
```

### OuterRadius <a href="#set_outer_radius" id="set_outer_radius"></a>

Задаёт внешний радиус.

Ожидается числовое значение.

```xml
<Object Name="SpinnerName">
  <Property Name="OuterRadius">25</Property>
</Object>
```

### ColorA <a href="#set_color_a" id="set_color_a"></a>

Задаёт название цвета первой полосы.

Ожидается название одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

```xml
<Object Name="SpinnerName">
  <Property Name="ColorA">#000000</Property>
</Object>
```

### ColorB <a href="#set_color_b" id="set_color_b"></a>

Задаёт название цвета последней полосы.

Ожидается название одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

```xml
<Object Name="SpinnerName">
  <Property Name="ColorB">#E6E6E6</Property>
</Object>
```
