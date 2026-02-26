---
description: Условный цвет фона ячейки.
---

# BackColor

## Шаблон BackColor <a href="#template" id="template"></a>

```xml
<BackColor Name="">
  <Color></Color>
  <ColorFromColumnValue></ColorFromColumnValue>
  <Columns>
    <Column Name="" />
    <Column Name="" />
  </Columns>
  <Expression></Expression>
  <Items>
    <Item></Item>
    <Item></Item>
  </Items>
</BackColor>
```

Цвет задается одним из способов с приоритетом выбора в следующем порядке:

1. Тэг [`<Color>`](back_color.md#color);
2. Тэг [`<ColorFromColumnValue>`](back_color.md#color_from_column_value);
3. Атрибут [`Name`](back_color.md#name).

## Атрибуты BackColor <a href="#attributes" id="attributes"></a>

### Name

Задает имя цвета для фона ячейки.

Необязательный атрибут. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

## Тэги BackColor <a href="#specific-tags" id="specific-tags"></a>

### Color <a href="#color" id="color"></a>

Задает имя цвета, описанного на форме.

Необязательный тэг. Ожидается имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

```xml
<Color>#E64A19</Color>
```

### ColorFromColumnValue <a href="#color_from_column_value" id="color_from_column_value"></a>

Задает имя столбца, в котором хранится название цвета.\
Игнорируется, если используется тэг [`<Color>`](back_color.md#color).&#x20;

Необязательный тэг. Ожидается имя одного из столбцов таблицы, в котором записано название цвета или цвет в формате HTML (#rrggbb).

```xml
<ColorFromColumnValue>ColumnName</ColorFromColumnValue>
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
Все поддерживаемые в выражении для вычисления конструкции смотрите по ссылке "[http://msdn.microsoft.com/en-us/library/system.data.datacolumn.expression.aspx](http://msdn.microsoft.com/en-us/library/system.data.datacolumn.expression.aspx)".
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
