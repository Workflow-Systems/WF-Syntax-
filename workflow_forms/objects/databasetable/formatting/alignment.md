---
description: Условное положение содержимого ячейки
---

# Alignment

## Шаблон Alignment <a href="#template" id="template"></a>

```xml
<Alignment Value="">
  <Value></Value>
  <Columns>
    <Column Name="" />
  </Columns>
  <Expression></Expression>
  <Items>
    <Item></Item>
  </Items>
</Alignment>
```

Положение задается одним из способов с приоритетом выбора в следующем порядке:

1. Тэг [`<Value>`](alignment.md#value);
2. Атрибут [`Value`](alignment.md#atr_value);

## Атрибуты Alignment <a href="#attributes" id="attributes"></a>

### Value <a href="#atr_value" id="atr_value"></a>

Задает название типа положения содержимого ячейки.

Необязательный атрибут. Ожидает название одного из типов положения:

<table data-header-hidden><thead><tr><th width="226.6296484971982" align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">NotSet</td><td>Значение наследуется от свойства <a href="alignment.md#column_headers_alignment"><code>&#x3C;ColumnHeadersAlignment></code></a> таблицы<br>(По умолчанию)</td></tr><tr><td align="center">TopLeft</td><td>Содержимое выравнивается по верхнему краю в вертикальном направлении и по левому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">TopCenter</td><td>Содержимое выравнивается по верхнему краю в вертикальном направлении и по центру ячейки</td></tr><tr><td align="center">TopRight</td><td>Содержимое выравнивается по верхнему краю в вертикальном направлении и по правому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">MiddleLeft</td><td>Содержимое выравнивается вертикально по середине и горизонтально по левому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">MiddleCenter</td><td>Содержимое выравнивается по вертикальному и горизонтальному центру ячейки</td></tr><tr><td align="center">MiddleRight</td><td>Содержимое выравнивается вертикально по середине и горизонтально по правому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">BottomLeft</td><td>Содержимое выравнивается по нижнему краю в вертикальном направлении и по левому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">BottomCenter</td><td>Содержимое выравнивается по нижнему краю в вертикальном направлении и по центру ячейки</td></tr><tr><td align="center">BottomRight</td><td>Содержимое выравнивается по нижнему краю в вертикальном направлении и по правому краю ячейки в горизонтальном направлении</td></tr></tbody></table>

## Тэги Alignment <a href="#specific-tags" id="specific-tags"></a>

### Value <a href="#value" id="value"></a>

Задает название типа положения содержимого ячейки.

Необязательный тэг. Ожидает название одного из типов положения:

<table data-header-hidden><thead><tr><th width="226.6296484971982" align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">NotSet</td><td>Значение наследуется от свойства <a href="alignment.md#column_headers_alignment"><code>&#x3C;ColumnHeadersAlignment></code></a> таблицы<br>(По умолчанию)</td></tr><tr><td align="center">TopLeft</td><td>Содержимое выравнивается по верхнему краю в вертикальном направлении и по левому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">TopCenter</td><td>Содержимое выравнивается по верхнему краю в вертикальном направлении и по центру ячейки</td></tr><tr><td align="center">TopRight</td><td>Содержимое выравнивается по верхнему краю в вертикальном направлении и по правому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">MiddleLeft</td><td>Содержимое выравнивается вертикально по середине и горизонтально по левому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">MiddleCenter</td><td>Содержимое выравнивается по вертикальному и горизонтальному центру ячейки</td></tr><tr><td align="center">MiddleRight</td><td>Содержимое выравнивается вертикально по середине и горизонтально по правому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">BottomLeft</td><td>Содержимое выравнивается по нижнему краю в вертикальном направлении и по левому краю ячейки в горизонтальном направлении</td></tr><tr><td align="center">BottomCenter</td><td>Содержимое выравнивается по нижнему краю в вертикальном направлении и по центру ячейки</td></tr><tr><td align="center">BottomRight</td><td>Содержимое выравнивается по нижнему краю в вертикальном направлении и по правому краю ячейки в горизонтальном направлении</td></tr></tbody></table>

```xml
<Value>MiddleCenter</Value>
```

### Columns <a href="#columns" id="columns"></a>

Столбцы таблицы, для которых распространяется условное форматирование ячеек.

Необязательный тэг. Ожидает список тэгов `<Column>`.

Если тэг `<Columns>` отсутствует, то условное форматирование распространяется на все столбцы таблицы.

```xml
<Columns>
  <Column Name="ColumnName1" />
  <Column Name="ColumnName2" />
</Columns>
```

Необязательный тэг `<Column>` имеет обязательный атрибут `Name`, ожидающий название одного из столбцов таблицы, на который распространяется условное форматирование ячеек.

### Expression <a href="#expression" id="expression"></a>

Выражение для вычисления, возвращающее логическое значение, на основе которого форматирование будет применено или нет.

Обязательный тэг. Ожидает любое значение.

```xml
<Expression>ColumnName3 > {0} * {1}</Expression>
```

Выражение для вычисления поддерживает выражения вида "ColumnName", где ColumnName - название одного из столбцов данной таблицы, и выражения вида "{N}" для подстановки значений (N+1)-ого элемента, то есть {0}, {1} и т. д.

{% hint style="info" %}
Все поддерживаемые в выражении для вычисления конструкции смотрите по ссылке "[http://msdn.microsoft.com/en-us/library/system.data.datacolumn.expression.aspx](http://msdn.microsoft.com/en-us/library/system.data.datacolumn.expression.aspx)
{% endhint %}

### Items <a href="#items" id="items"></a>

Переменные для подстановки в выражение для вычисления.

Необязательный тэг. Ожидает список тэгов `<Item>`.

```xml
<Items>
  <Item>10</Item>
  <Item>20</Item>
</Items>
```

Необязательный тэг `<Item>` ожидает любое значение.
