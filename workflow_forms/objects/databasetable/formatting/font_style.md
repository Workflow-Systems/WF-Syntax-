---
description: Условный стиль шрифта ячейки
---

# FontStyle

## Шаблон FontStyle <a href="#template" id="template"></a>

```xml
<FontStyle Name="">
  <Columns>
    <Column Name="" />
    <Column Name="" />
  </Columns>
  <Expression></Expression>
  <Items>
    <Item></Item>
    <Item></Item>
  </Items>
</FontStyle>
```

## Атрибуты FontStyle <a href="#attributes" id="attributes"></a>

### Name

Задает имя стиля для шрифта ячейки. Стиль должен быть описан на форме.

Обязательный атрибут. Любое значение будет переведено в текстовое

## Тэги FontStyle <a href="#specific-tags" id="specific-tags"></a>

### Columns <a href="#columns" id="columns"></a>

Столбцы таблицы, для которых распространяется условное форматирование ячеек.

Необязательный тэг. Ожидает список тэгов [`<Column>`](font_style.md#formatting_fore_color_columns_column).

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
