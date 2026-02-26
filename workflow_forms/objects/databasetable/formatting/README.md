---
description: >-
  Условное форматирование ячеек таблицы на основе значений других ячеек таблицы
  в этой же строке.
---

# Formatting

## Шаблон Formatting <a href="#template" id="template"></a>

```xml
<Formatting>
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
  <ForeColor Name="">
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
  </ForeColor>
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
  <Alignment>
    <Value>MiddleCenter</Value>
    <Columns>
      <Column Name="ColumnName1" />
    </Columns>
    <Expression>ColumnName3 > {0}</Expression>
    <Items>
      <Item>10</Item>
    </Items>
  </Alignment>
  <Alignment Value="MiddleRight">
    <Columns>
      <Column Name="ColumnName2" />
    </Columns>
    <Expression>ColumnName4</Expression>
  </Alignment>
</Formatting>
```

## Тэги Formatting <a href="#specific-tags" id="specific-tags"></a>

### BackColor <a href="#back_color" id="back_color"></a>

Условный цвет фона ячейки.

Необязательный тэг. Описание вложенных тэгов по [ссылке](back_color.md).

Необязательный атрибут `Name` ожидает имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

```xml
<BackColor Name="BackColor">
  <Columns>
    <Column Name="ColumnName1" />
    <Column Name="ColumnName2" />
  </Columns>
  <Expression>ColumnName3 > {0} * {1}</Expression>
  <Items>
    <Item>10</Item>
    <Item>20</Item>
  </Items>
</BackColor>
```

### ForeColor <a href="#fore_color" id="fore_color"></a>

Условный цвет шрифта ячейки.

Необязательный тэг. Описание вложенных тэгов по [ссылке](fore_color.md).

Необязательный атрибут `Name` ожидает имя одного из цветов, описанных на форме или описание цвета в формате HTML (#rrggbb).

```xml
<ForeColor Name="ForeColor">
  <Columns>
    <Column Name="ColumnName1" />
    <Column Name="ColumnName2" />
  </Columns>
  <Expression>ColumnName3 > {0} * {1}</Expression>
  <Items>
    <Item>10</Item>
    <Item>20</Item>
  </Items>
</ForeColor>
```

### FontStyle <a href="#font_style" id="font_style"></a>

Условный стиль шрифта ячейки.

Необязательный тэг. Описание вложенных тэгов по [ссылке](font_style.md).

Обязательный атрибут `Name` ожидает имя одного из стилей шрифтов, описанных на форме.

```xml
<FontStyle Name="FontStyle">
  <Columns>
    <Column Name="ColumnName1" />
    <Column Name="ColumnName2" />
  </Columns>
  <Expression>ColumnName3 > {0} * {1}</Expression>
  <Items>
    <Item>10</Item>
    <Item>20</Item>
  </Items>
</FontStyle>
```

### Alignment <a href="#alignment" id="alignment"></a>

Условное положение содержимого ячейки.

Необязательный тэг. Описание вложенных тэгов по [ссылке](alignment.md).

Необязательный атрибут `Value` ожидает название одного из типов положения:

<table data-header-hidden><thead><tr><th width="223.76049129989767" align="center"></th><th width="437.3333333333333"></th></tr></thead><tbody><tr><td align="center">TopLeft</td><td>Слева сверху</td></tr><tr><td align="center">TopCenter</td><td>По центру сверху</td></tr><tr><td align="center">TopRight</td><td>Справа сверху</td></tr><tr><td align="center">MiddleLeft</td><td>Слева посередине</td></tr><tr><td align="center">MiddleCenter</td><td>По центру посередине</td></tr><tr><td align="center">MiddleRight</td><td>Справа посередине</td></tr><tr><td align="center">BottomLeft</td><td>Слева снизу</td></tr><tr><td align="center">BottomCenter</td><td>По центру снизу</td></tr><tr><td align="center">BottomRight</td><td>Справа снизу</td></tr></tbody></table>

```xml
<Alignment Value="MiddleRight">
  <Columns>
    <Column Name="ColumnName2" />
  </Columns>
  <Expression>ColumnName3 > {0}</Expression>
  <Items>
    <Item>10</Item>
  </Items>
</Alignment>
```
