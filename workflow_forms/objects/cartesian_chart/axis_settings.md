---
description: >-
  Задает настройки осей для диаграммы типы CartesianChart - столбчатая/линейная
  диаграмма.
---

# AxisSettings

## Шаблон AxisSettings <a href="#template" id="template"></a>

```xml
<AxisSettings SecondaryAxisType="Text">
  <XAxisRotation></XAxisRotation>
  <YAxisRotation></YAxisRotation>
  <XAxisColor></XAxisColor>
  <YAxisColor></YAxisColor>
  <ShowXSeparator></ShowXSeparator>
  <ShowYSeparator></ShowYSeparator>
  <MinXValue></MinXValue>
  <MaxXValue></MaxXValue>
  <MinYValue></MinYValue>
  <MaxYValue></MaxYValue>
  <MinXStep></MinXStep>
  <MinYStep></MinYStep>
  <MainAxisLabels></MainAxisLabels>
</AxisSettings>
```

## Атрибуты AxisSettings <a href="#attributes" id="attributes"></a>

### SecondaryAxisType  <a href="#secondary_axis_type" id="secondary_axis_type"></a>

Задает тип отображаемых данных на вторичной оси.

Необязательный атрибут. Ожидается одно из значений: Double, Text. По умолчанию используется значение Double.

{% hint style="info" %}
Вторичной осью является ось X, расположенная горизонтально. Вертикальная ось, ось Y, является основной.
{% endhint %}

## Тэги AxisSettings <a href="#specific-tags" id="specific-tags"></a>

### XAxisRotation <a href="#x_axis_rotation" id="x_axis_rotation"></a>

Задает угол поворота текста на оси X.

Необязательный тег. Ожидается целое число.

По умолчанию используется значение 0.

```xml
<XAxisRotation>0</XAxisRotation>
```

### YAxisRotation <a href="#y_axis_rotation" id="y_axis_rotation"></a>

Задает угол поворота текста на оси Y.

Необязательный тег. Ожидается целое число.

По умолчанию используется значение 0.

```xml
<YAxisRotation>0</YAxisRotation>
```

### XAxisColor <a href="#x_axis_color" id="x_axis_color"></a>

Задает цвет текста на оси X.

Необязательный тег. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется черный цвет.

```xml
<XAxisColor>SoftBlue</XAxisColor>
```

### YAxisColor <a href="#y_axis_color" id="y_axis_color"></a>

Задает цвет текста на оси Y.

Необязательный тег. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется черный цвет.

```xml
<YAxisColor>SoftBlue</YAxisColor>
```

### ShowXSeparator <a href="#show_x_separator" id="show_x_separator"></a>

Задает видимость линий сетки оси X.

Необязательный тег. Ожидается логическое значение.

По умолчанию используется значение True.

```xml
<ShowXSeparator>True</ShowXSeparator>
```

### ShowYSeparator <a href="#show_y_separator" id="show_y_separator"></a>

Задает видимость линий сетки оси Y.

Необязательный тег. Ожидается логическое значение.

По умолчанию используется значение True.

```xml
<ShowYSeparator>True</ShowYSeparator>
```

### MinXValue <a href="#min_x_value" id="min_x_value"></a>

Задает минимальное значение по оси X.

Необязательный тег. Ожидается число.

По умолчанию ограничения нет.

```xml
<MinXValue>0</MinXValue>
```

### MaxXValue <a href="#max_x_value" id="max_x_value"></a>

Задает максимальное значение по оси X.

Необязательный тег. Ожидается число.

По умолчанию ограничения нет.

```xml
<MaxXValue>100</MaxXValue>
```

### MinYValue <a href="#min_y_value" id="min_y_value"></a>

Задает минимальное значение по оси Y.

Необязательный тег. Ожидается число.

По умолчанию ограничения нет.

```xml
<MinYValue>0</MinYValue>
```

### MaxYValue <a href="#max_y_value" id="max_y_value"></a>

Задает максимальное значение по оси Y.

Необязательный тег. Ожидается число.

По умолчанию ограничения нет.

```xml
<MaxYValue>1000</MaxYValue>
```

### MinXStep <a href="#min_x_step" id="min_x_step"></a>

Задает минимальный шаг оси X.

Необязательный тег. Ожидается число.

По умолчанию используется значение 0.

```xml
<MinXStep>1</MinXStep>
```

### MinYStep <a href="#min_y_step" id="min_y_step"></a>

Задает минимальный шаг оси Y.

Необязательный тег. Ожидается число.

По умолчанию используется значение 0.

```xml
<MinYStep>100</MinYStep>
```

### MainAxisLabels

Задает отображаемые значения по основной (числовой) оси (Х – для типа Row, Y – для остальных).

Необязательный тег. Ожидается массив строк.

```xml
<MainAxisLabels>
  <Structure Type="List">
    <Item>Item1</Item>
    <Item>Item2</Item>
  </Structure>
</MainAxisLabels>
```
