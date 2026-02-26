---
description: Столбчатая или линейная диаграмма. Элемент пользовательского интерфейса.
---

# CartesianChart

## Шаблон CartesianChart <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="" Type="CartesianChart" Assembly="BaseControls" ChangeForm="">
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
  <!--Тэги, специфичные для CartesianChart-->
  <SortDirection></SortDirection>
  <SortData></SortData>
  <LegendPosition></LegendPosition>
  <LegendTextSize></LegendTextSize>
  <TooltipTextSize></TooltipTextSize>
  <StrokeThickness></StrokeThickness>
  <ZoomMode></ZoomMode>
  <AxisSettings SecondaryAxisType="">
    <XAxisRotation></XAxisRotation>
    <YAxisRotation></YAxisRotation>
    <XAxisColor></XAxisColor>
    <YAxisColor></YAxisColor>
    <ShowXSeparator></ShowXSeparator>
    <ShowYSeparator></ShowYSeparator>
    <MinXValue></MinXValue>
    <MAxXValue></MaxXValue>
    <MinYValue></MinYValue>
    <MaxYValue></MaxYValue>
    <MinXStep></MinXStep>
    <MinYStep></MinYStep>
    <MainAxisLabels></MainAxisLabels>
  </AxisSettings>
  <SeriesCollection Type="">
    <Series Name="" Color="">
      <Title></Title>
      <Points></Points>
      <Visible></Visible>
    </Series>
  </SeriesCollection>
</MyObject>
```

## Описание CartesianChart <a href="#description" id="description"></a>

```xml
<MyObject Name="CartesianChartName" Type="CartesianChart" Assembly="BaseControls">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для CartesianChart-->
</MyObject>
```

CartesianChart не имеет значения.

## Тэги, специфичные для CartesianChart <a href="#specific-tags" id="specific-tags"></a>

### SortDirection <a href="#sort_direction" id="sort_direction"></a>

Задает направление сортировки данных по оси Y, которая является основной.

Необязательный тэг. Ожидается одно из значений:

<table data-header-hidden><thead><tr><th width="197"></th><th></th></tr></thead><tbody><tr><td>Asc </td><td>По возрастанию</td></tr><tr><td>Desc </td><td>По убыванию</td></tr></tbody></table>

По умолчанию используется значение Desc.

```xml
<SortDirection>Desc</SortDirection>
```

### SortData <a href="#sort_data" id="sort_data"></a>

Задает имя серии, по которой необходимо сортировать данные.

Необязательный тэг. Ожидается имя одной из указанных серий (атрибут [`Name`](series.md#name) тэга [`<Series>`](series.md)).

```xml
<SortData>SeriaName</SortData>
```

### LegendPosition <a href="#legend_position" id="legend_position"></a>

Задает положение легенды графика.

Необязательный тег. Ожидается одно из значений:

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

### TooltipTextSize <a href="#tool_tip_text_size" id="tool_tip_text_size"></a>

Задает размер шрифта всплывающих подсказок на диаграмме.

Необязательный тэг. Ожидается положительно целое число.

По умолчанию используется значение 12.

```xml
<TooltipTextSize>13</TooltipTextSize>
```

### StrokeThickness <a href="#stroke_thickness" id="stroke_thickness"></a>

Задает толщину границ сегментов диаграммы.

Необязательный тэг. Ожидается число.

По умолчанию используется значение 0.

```xml
<StrokeThickness>2</StrokeThickness>
```

### ZoomMode <a href="#zoom_mode" id="zoom_mode"></a>

Задает режим приближения и отдаления графика.

Необязательный тэг. Ожидается одно из значений:

<table data-header-hidden><thead><tr><th width="202.08667435984262" align="center"></th><th width="521.8817842146913"></th></tr></thead><tbody><tr><td align="center">None</td><td>Режим приближения и отдаления выключен.</td></tr><tr><td align="center">X</td><td>Режим приближения и отдаления только по оси X (вторичная ось).</td></tr><tr><td align="center">Y</td><td>Режим приближения и отдаления только по оси Y (основная ось).</td></tr><tr><td align="center">Both</td><td>Режим приближения и отдаления только по обеим осям.</td></tr></tbody></table>

По умолчанию используется значение None.

```xml
<ZoomMode>None</ZoomMode>
```

### AxisSettings <a href="#axis_settings" id="axis_settings"></a>

Задает настройки осей.

Необязательный тэг.  Описание вложенных тэгов по [ссылке](axis_settings.md).

```xml
<AxisSettings SecondaryAxisType="Text">
  <XAxisRotation>0</XAxisRotation>
  <YAxisRotation>0</YAxisRotation>
  <XAxisColor>SoftBlue</XAxisColor>
  <YAxisColor>SoftBlue</YAxisColor>
  <ShowXSeparator>True</ShowXSeparator>
  <ShowYSeparator>True</ShowYSeparator>
  <MinXValue>0</MinXValue>
  <MAxXValue>100</MaxXValue>
  <MinYValue>0</MinYValue>
  <MaxYValue>1000</MaxYValue>
  <MinXStep>1</MinXStep>
  <MinYStep>100</MinYStep>
  <MainAxisLabels>
    <Structure Type="List">
      <Item>Item1</Item>
      <Item>Item2</Item>
    </Structure>
  </MainAxisLabels>
</AxisSettings>
```

Необязательный атрибут `SecondaryAxisType` задает тип отображаемых данных на вторичной оси. Ожидается одно из значений: Double, Text. По умолчанию используется значение Double.

{% hint style="info" %}
Вторичной осью является ось X, расположенная горизонтально. Вертикальная ось, ось Y, является основной.
{% endhint %}

### SeriesCollection <a href="#series_collection" id="series_collection"></a>

Задает данные для отображения графиков.

Обязательный тэг. Ожидает список тэгов [`<Series>`](series.md).

```xml
<SeriesCollection Type="Row">
  <Series Name="SeriaName" Color="Green">
    <Title>Имя серии</Title>
    <Points>
      <DataConnection SourceDataConnection="PrimaryGetDataConnection">
        <Fields>
          <Field Name="MainAxisTextValue" />
          <Field Name="MainAxisValue" />
          <Field Name="Hint" />
        </Fields>
      </DataConnection>
    </Points>
    <Visible>True</Visible>
  </Series>
</SeriesCollection>
```

Обязательный атрибут `Type` задает тип графика. Ожидается одно из значений:

<table data-header-hidden><thead><tr><th width="202.08667435984262" align="center"></th><th width="521.8817842146913"></th></tr></thead><tbody><tr><td align="center">Line</td><td>Линейная диаграмма.</td></tr><tr><td align="center">Row</td><td>Полосовая диаграмма (столбики расположены горизонтально).</td></tr><tr><td align="center">Column</td><td>Столбчатая диаграмма (столбики расположены вертикально).</td></tr></tbody></table>

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### GetImage <a href="#get_get_image" id="get_get_image"></a>

Возвращает путь до файла изображения графика в папке Temp.

```xml
<Object Name="CartesianChartName">
  <Property Name="GetImage" />
</Object>
```

### OpenImage <a href="#get_open_image" id="get_open_image"></a>

Открывает изображение графика из папки Temp в стандартном средстве просмотра фотографий.

```xml
<Object Name="CartesianChartName">
  <Property Name="OpenImage" />
</Object>
```
