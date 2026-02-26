---
description: Круговая диаграмма. Элемент пользовательского интерфейса.
---

# PieChart

## Шаблон PieChart <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="" Type="PieChart" Assembly="BaseControls" ChangeForm="">
  <!--Тэги, общие для всех графических объектов-->
  <Top></Top>
  <Bottom></Bottom>
  <Left></Left>
  <Right></Right>
  <Height></Height>
  <Width></Width>
  <BackColor></BackColor>
  <Enabled></Enabled>
  <Visible></Visible>
  <Hint></Hint>
  <Change User="" Source="" ValueSet="" />
  <!--Тэги, специфичные для PieChart-->
  <LegendPosition></LegendPosition>
  <LegendTextSize></LegendTextSize>
  <DataLabelsPosition></DataLabelsPosition>
  <InnerRadius></InnerRadius>
  <StrokeThickness></StrokeThickness>
  <StrokeColor></StrokeColor> 
  <Series><Series>
</MyObject>
```

## Описание PieChart <a href="#description" id="description"></a>

```xml
<MyObject Name="PieChartName" Type="PieChart" Assembly="BaseControls">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для PieChart-->
</MyObject>
```

PieChart не имеет значения.

## Тэги, специфичные для PieChart <a href="#specific-tags" id="specific-tags"></a>

### LegendPosition <a href="#legend_position" id="legend_position"></a>

Задает положение легенды диаграммы.

Необязательный тэг. Ожидается одно из значений:

<table data-header-hidden><thead><tr><th width="202.08667435984262" align="center"></th><th width="521.8817842146913"></th></tr></thead><tbody><tr><td align="center">Left</td><td>Легенда слева от графика.</td></tr><tr><td align="center">Right</td><td>Легенда справа от графика.</td></tr><tr><td align="center">Top</td><td>Легенда над графиком.</td></tr><tr><td align="center">Bottom</td><td>Легенда под графиком.</td></tr><tr><td align="center">Hidden</td><td>Легенда не отображается.</td></tr></tbody></table>

По умолчанию используется значение Hidden.

```xml
<LegendPosition>Hidden</LegendPosition>
```

### LegendTextSize <a href="#legend_text_size" id="legend_text_size"></a>

Задает размер шрифта в легенде диаграммы.

Необязательный тэг. Ожидается положительно целое число.

По умолчанию используется значение 15.

```xml
<LegendTextSize>13</LegendTextSize>
```

### DataLabelsPosition <a href="#data_labels_position" id="data_labels_position"></a>

Задает положение подписей сегментов диаграммы.

Необязательный тэг. Ожидается одно из значений:

<table data-header-hidden><thead><tr><th width="202.08667435984262" align="center"></th><th width="521.8817842146913"></th></tr></thead><tbody><tr><td align="center">ChartCenter</td><td>Размещает подпись в центре диаграммы.</td></tr><tr><td align="center">End</td><td>Выравнивает подпись по концу угла сегмента.</td></tr><tr><td align="center">Start</td><td>Выравнивает подпись по началу угла сегмента.</td></tr><tr><td align="center">Middle</td><td>Выравнивает подпись по середине угла внутри сегмента.</td></tr><tr><td align="center">Outer</td><td>Выравнивает подпись по середине угла вне сегмента.</td></tr></tbody></table>

По умолчанию используется значение Outer.

```xml
<DataLabelsPosition>Outer</DataLabelsPosition>
```

### DataLabelsTextSize <a href="#data_labels_text_size" id="data_labels_text_size"></a>

Задает размер шрифта подписи сегмента диаграммы.

Необязательный тэг. Ожидается положительно целое число.

По умолчанию используется значение 16.

```xml
<DataLabelsTextSize>13</DataLabelsTextSize>
```

### TooltipTextSize <a href="#tool_tip_text_size" id="tool_tip_text_size"></a>

Задает размер шрифта всплывающих подсказок на диаграмме.

Необязательный тэг. Ожидается положительно целое число.

По умолчанию используется значение 12.

```xml
<TooltipTextSize>13</TooltipTextSize>
```

### InnerRadius <a href="#inner_radius" id="inner_radius"></a>

Задает внутренний радиус круговой диаграммы.

Необязательный тэг. Ожидается число.

По умолчанию используется значение 0.

```xml
<InnerRadius>0</InnerRadius>
```

### StrokeThickness <a href="#stroke_thickness" id="stroke_thickness"></a>

Задает толщину границ сегментов диаграммы.

Необязательный тэг. Ожидается число.

По умолчанию используется значение 0.

```xml
<StrokeThickness>0</StrokeThickness>
```

### StrokeColor <a href="#stroke_color" id="stroke_color"></a>

Задает цвет границ сегментов диаграммы.

Необязательный тэг. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

По умолчанию равен цвету сегмента диаграммы из тэга `<Series>`.

```xml
<StrokeColor>0</StrokeColor>
```

### Series

Задает данные для построения и отображения диаграммы.

Обязательный тэг. Ожидается матрица с 5 столбцами:

* Наименование значения (текст). Обязательный.
* Значение (double). Обязательный.
* Текст подсказки при наведении на сегмент диаграммы. Необязательный. По умолчанию формируется строка из наименования и значения.
* Цвет сегмента диаграммы. Необязательный. Ожидается имя цвета или описание цвета в формате HTML (#rrggbb). По умолчанию голубой.
* Текст подписи сегмента диаграммы (текст). Необязательный.

```xml
<Series>
  <DataConnection SourceDataConnection="PrimaryGetDataConnection">
    <Fields>
      <Field Name="MainAxisTextValue" />
      <Field Name="MainAxisValue" />
      <Field Name="Hint" />
      <Field Name="Color" />
      <Field Name="DataLabels" />
    </Fields>
  </DataConnection>
</Series>
```

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### GetImage <a href="#get_get_image" id="get_get_image"></a>

Возвращает путь до файла изображения графика в папке Temp.

```xml
<Object Name="PieChartName">
  <Property Name="GetImage" />
</Object>
```

### OpenImage <a href="#get_open_image" id="get_open_image"></a>

Открывает изображение графика из папки Temp в стандартном средстве просмотра фотографий.

```xml
<Object Name="PieChartName">
  <Property Name="OpenImage" />
</Object>
```
