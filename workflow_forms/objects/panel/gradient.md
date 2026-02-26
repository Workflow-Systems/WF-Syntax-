---
description: Задает настройки градиентной заливки панель.
---

# Gradient

## Шаблон Gradient <a href="#template" id="template"></a>

```xml
<Gradient>
  <StartColor></StartColor>
  <FinishColor></FinishColor>
  <Scale></Scale>
  <Mode></Mode>
</Gradient>
```

## Тэги Gradient <a href="#specific-tags" id="specific-tags"></a>

### StartColor <a href="#start_color" id="start_color"></a>

Задает начальный цвет градиента.

Необязательный тег. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется Transparent (прозрачный).

```xml
<StartColor>#8BC34A</StartColor>
```

### FinishColor <a href="#finish_color" id="finish_color"></a>

Задает конечный цвет градиента.

Необязательный тег. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется Transparent (прозрачный).

```xml
<FinishColor>#FBC02D</FinishColor>
```

### Scale <a href="#scale" id="scale"></a>

Задает в процентах силу перехода начального цвета в конечный

Необязательный тег. Ожидается целочисленное положительное число.

По умолчанию используется значение 0.

```xml
<Scale>100</Scale>
```

### Mode <a href="#mode" id="mode"></a>

Задает направление перехода цветов.

Необязательный тэг. Ожидается название одного из направлений перехода цветов:

<table data-header-hidden><thead><tr><th width="193" align="center"></th><th></th></tr></thead><tbody><tr><td align="center">Horizontal</td><td>Линейный градиент слева направо</td></tr><tr><td align="center">Vertical</td><td>Линейный градиент сверху вниз</td></tr><tr><td align="center">BackwardDiagonal</td><td>Диагональный градиент из верхнего правого в нижний левый</td></tr><tr><td align="center">ForwardDiagonal</td><td>Диагональный градиент из верхнего левого в нижний правый</td></tr></tbody></table>

По умолчанию используется значение Horizontal.

```xml
<Mode>BackwardDiagonal</Mode>
```
